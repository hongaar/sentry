<a id="addGroup"></a>
###addGroup($group)

----------

Assign a user to a group.

Parameters                   | Type            | Default       | Description
:--------------------------- | :-------------: | :------------ | :--------------
`$group`                     | GroupInterface  | none          | GroupInterface instance

`returns` void
`throws` GroupNotFoundException

####Example

	try
	{
		$user  = Sentry::getUserProvider()->findById(1);
		$group = Sentry::getGroupProvider()->findById(1);

		$user->addGroup($group);
	}
	catch (Cartalyst\Sentry\Users\UserNotFoundException $e)
	{
		echo 'User does not exist.';
	}
	catch (Cartalyst\Sentry\Groups\GroupNotFoundException $e)
	{
		echo 'Group does not exist.';
	}