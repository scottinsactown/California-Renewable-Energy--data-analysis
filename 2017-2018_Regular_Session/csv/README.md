# LegiScan Public Datasets

## CSV Datasets
See [LegiScan Datasets](https://legiscan.com/datasets) for more information.

## bills.csv
List of bills and their basic details along with links to LegiScan and state pages.

	bill_number - Bill number
	bill_id - LegiScan bill identifier
	session_id - LegiScan session identifier
	status - Status value for bill
	status_desc - Description of bill status value
	status_date - Date of status change
	title - Short title of bill
	description - Long title of bill
	committee_id - LegiScan committee identifier
	committee - Pending committee name
	last_action_date - Date of last action
	last_action - Description of last action
	url - LegiScan URL for bill detail
	state_link - State URL for bill detail

## history.csv
List of history steps / actions taken, keyed to `bills.csv` by `bill_id`.

	bill_id - LegiScan bill identifier
	date - Date of history step
	chamber - Chamber the action occurred in
	sequence - Ordered sequence of history step
	action - Description of history step

## people.csv
List of legisltors and their basic details along with third party identifiers.

	people_id - LegiScan person identifier
	name - Full name
	first_name - First name
	middle_name - Middle name
	last_name - Last name
	suffix - Suffix
	nickname - Nickname
	party_id - LegiScan political party identifier
	party - Political party descirption
	role_id - LegiScan legislative role identifier
	role - Legilsative role description
	district - Legislative district
	followthemoney - Identifier for [Follow The Money](https://www.followthemoney.org/)
	votesmart - Identifier for [Vote Smart](https://votesmart.org/)
	opensecrets - Identifier for [OpenSecrets](https://www.opensecrets.org/)
	ballotpedia - Identifier for [Ballotpedia](https://ballotpedia.org/)

## rollcalls.csv
List of roll calls for each bill, keyed to `bills.csv` by `bill_id`.

	bill_id - LegiScan bill identifier
	roll_call_id - LegiScan roll call identifier
	date - Date of the roll call
	chamber - Chamber the roll call occurred in
	description - Description of the roll call
	yea - Number of Yeas
	nay - Number of Nays
	nv - Number of NV/Abstains
	absent - Number of Absences
	total - Total votes

## sponsors.csv
List of sponsors for each bill, keyed to `bills.csv` and `people.csv` by `bill_id`
and `people_id` respectively.

	bill_id - LegiScan bill identifier
	people_id - LegiScan person identifer
	position - Ordered position of the sponsor in list

## votes.csv
List of individual vote details for each roll call, keyed to `rollcalls.csv` and
`people.csv` by `roll_call_id` and `people_id` respectively.

	roll_call_id - LegiScan roll call identifier
	people_id - LegiScan person identifier
	vote - Vote value
	vote_desc - Vote description