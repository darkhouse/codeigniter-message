CodeIgniter Message
===================

This library is an easy to use interface to CodeIgniter's flash data, aimed at providing informational messages to the user.

Usage
-----

Load the Message library.

    $this->load->library('message');

Write an error message. You can exchange the message type ("error", in the case below), for whatever you like. This can be used to style the HTML output of the library in a view.

    $this->message->set('error', 'This item couldn\'t be deleted.');

Write an error message in the "item" group and preserve the message for one additional request.

    $this->message->set('error', 'This item couldn\'t be deleted.', TRUE, 'item');

Get all messages (in a view).
	
	echo $this->message->display();

Or get all messages from a specific group.

	echo $this->message->display('item');
	
You can also specify a wrapper, which is wrapped(!) around the message(s). You can also specify a global wrapper in the config.

	echo $this->message->display('item', array('<div class="messages">', '</div>'));