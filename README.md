# php_mysql_parser
PHP's favorite MySQL parser!

## Goals

* Must be able to import php_mysql_parser by requiring a single PHP file
* Library must be written in pure PHP (however, I'm open to using parser generators to create the library)
* Must adhere to MySQL official grammar (except where implementation details require modifications)

There are other design goals, but these are the big 3. Also, as a preference, I'd like it if users didn't have to use composer or any additional install tools.  Just download the needed files and require the entry point.

## How to use

    // "easy" way:
    $syntax_tree = MySQLParser\Parser::parse_string("SELECT 1;");

    // "hard" way:
    $lexer = new MySQLParser\Lexer("SELECT 1;");
    $syntax_tree = MySQLParser\Parser::parse($lexer);
    
    
## How to install
Pretty easy:

    git clone https://github.com/jameslaydigital/php_mysql_parser
    ## in PHP... #
    require("MySQLParser.php");

## Additional Notes
This library is currently not finished, and even when it is, it will not be optimized for performance for some time.  I want to get this thing up and running with minimal effort.
