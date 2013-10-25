### a-tools

Cross-browser text selection and modification plugin built on top of the jQuery library. Tested with Opera 9.5 (Windows) and Opera 9.6 (Linux), Mozilla Firefox 3.0 (Windows and Linux), Internet Explorer 7, Chrome 2.0 and Safari 4.0. Also works with jQuery 1.4.

Plugin could work with multiple elements of «textarea» or «input type=text».

This plugin has seven functions:

	getSelection – return start, end position, length of the selected text and the selected text. 
	return start=end=caret position if text is not selected;
	
	replaceSelection – replace selected text with a given string;
	
	setSelection – select text in a given range (startPosition and endPosition);
	
	countCharacters – count amount of all characters;
	
	insertAtCaretPos – insert text at current caret position;
	
	setCaretPos – set cursor at caret position (1 = beginning, -1 = end);
	
	setMaxLength – set maximum length of input field. Also provides callback function if limit is reached.
	Note: The function has to have a number as input. Positive value for setting of limit and negative number for removing of limit.

### Syntaxes:

getSelection

	var obj = $("textarea").getSelection();
	var startPosition = obj.start;
	var endPosition = obj.end;
	var length = obj.length;
	var selectedText = obj.text;
	replaceSelection
	$("input").replaceSelection("Hello world");

Set Selection

	$("#textArea").setSelection(10,15);

countCharacters

	$("textarea").countCharacters();

insertAtCaretPos

	$("#textarea").insertAtCaretPos("Hello world");

setCaretPos

	$("#textArea").setCaretPos(10);

setMaxLength
Without callback function:

	$("textarea").setMaxLength(7);

With callback function which will return «Alert» when user will try to put one more symbol:

	$("textarea").setMaxLength(10, function() {
		alert("hello")
	});

Removing limit:

	$("textarea").setMaxLength(-1);

Try out a demonstration right now:
http://www.ampparit.com/projects/a-tools/demo.html

Please, do not hesitate to leave a comment or send feedback to the company
www.ampparit.com/tietoa/english