Monitio
=======

I am not adding fields like id because it should be clear that they are needed :)

User:
	char	name
	char	surname
	char	login
	char	password

Calendar:
	char	  calendarType
	m2m	    usersAssigned (user)
	date	  createdDate
	foreign	createdBy (user)

Item:
	foreign	calendar
	m2m	    concerns (user)
	date	  beginDate
	date	  endDate
	char	  description
	char	  type (Event, Task, Note)
	date	  createdDate
	foreign	createdBy (user)
