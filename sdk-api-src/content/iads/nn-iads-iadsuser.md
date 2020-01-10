---
UID: NN:iads.IADsUser
title: IADsUser (iads.h)
description: The IADsUser interface is a dual interface that inherits from IADs.
old-location: adsi\iadsuser.htm
tech.root: adsi
ms.assetid: 6eea74c2-2d6d-4dfd-9a22-3da2d5ce49bf
ms.date: 12/05/2018
ms.keywords: IADsUser, IADsUser interface [ADSI], IADsUser interface [ADSI],described, _ds_iadsuser, adsi.iadsuser, iads/IADsUser
f1_keywords:
- iads/IADsUser
dev_langs:
- c++
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Activeds.dll
api_name:
- IADsUser
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsUser interface


## -description


The <b>IADsUser</b> interface is a dual interface that inherits from  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is designed to represent and manage an end-user account on a network. Call the methods of this interface to access and manipulate end-user account data. Such data includes names of the user, telephone numbers, job title, and so on. This interface supports features for determining the group association of the user, and for setting or changing the password.
   

To bind to a domain user through a WinNT provider, use the domain name as part of the ADsPath, as shown in the following code example.

```cpp
GetObject("WinNT://MYDOMAIN/jeffsmith,user")
```

Similarly, use the computer name as part of the ADsPath to bind to a local user.

```cpp
GetObject("WinNT://MYCOMPUTER/jeffsmith,user")
```

In Active Directory, domain users reside in the directory. The following code example shows how to bind to a domain user through an LDAP provider.

```cpp
GetObject("LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com")
```

However, local accounts reside in the local SAM database and the LDAP provider does not communicate with the local database. Thus, to bind to a local user, you must go through a WinNT provider as described in the second code example.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsUser</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsUser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsUser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsuser-changepassword">ChangePassword</a>
</td>
<td align="left" width="63%">
Changes password from the specified existing value to a new value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-get">Get</a>
</td>
<td align="left" width="63%">
Gets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getex">GetEx</a>
</td>
<td align="left" width="63%">
Gets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getinfo">GetInfo</a>
</td>
<td align="left" width="63%">
Loads the property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getinfoex">GetInfoEx</a>
</td>
<td align="left" width="63%">
Loads specific property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsuser-groups">Groups</a>
</td>
<td align="left" width="63%">
Determines the groups to which this end-user belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-put">Put</a>
</td>
<td align="left" width="63%">
Sets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-putex">PutEx</a>
</td>
<td align="left" width="63%">
Sets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-setinfo">SetInfo</a>
</td>
<td align="left" width="63%">
Persists the changes on this object to the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsuser-setpassword">SetPassword</a>
</td>
<td align="left" width="63%">
Sets the password.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsUser</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">AccountDisabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the flag to indicate whether the account is disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">AccountExpirationDate</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the expiration date and time of the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">AdsPath</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the object's ADsPath that uniquely identifies this object from all others.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">BadLoginAddress</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the address of the last node, considered an "Intruder".

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">BadLoginCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of the bad logon attempts since last reset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">Class</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the name of the object's schema class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">Department</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the organizational unit within the organization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the description of the user account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">Division</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the division within a company (organization).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">EmailAddress</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the email address of the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">EmployeeID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets employee identification number of the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">FaxNumber</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the list of fax phone numbers. In Active Directory the list has a single element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">FirstName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the first name of the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">FullName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the full name of the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">GraceLoginsAllowed</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the number of times user can log on after password has expired.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">GraceLoginsRemaining</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the number of grace logins left before locking account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">GUID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the GUID of the object as stored in the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">HomeDirectory</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the home directory of the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">HomePage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the URL to the home page of the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">IsAccountLocked</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a flag to indicate whether an account is locked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">Languages</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the array of language names for the end-user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">LastFailedLogin</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the date and time of the last failed network login.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">LastLogin</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the date and time of the last network login.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">LastLogoff</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the date and time of the last network logoff.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">LastName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the last name of the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">LoginHours</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the time periods during each day of week that indicate valid login periods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">LoginScript</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the end-user's login script path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">LoginWorkstations</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and set the workstations and their net addresses for this end-user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">Manager</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the manager of the  user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">MaxLogins</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the maximum number of simultaneous logins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">MaxStorage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and set the maximum amount of disk space allotted for the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the object's relative name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">NamePrefix</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the name prefix, such as Mr., Ms., or Hon., of the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">NameSuffix</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the name suffix, such as Jr. or III, of the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">OfficeLocations</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the array of end-user locations. In Active Directory the array has a single element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">OtherName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the additional name, such as the nickname, or the middle name of the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">Parent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the ADsPath string for the parent of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">PasswordExpirationDate</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the date and time when password expires.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">PasswordLastChanged</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the date and time of the last password change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">PasswordMinimumLength</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the minimum number of characters allowed in a password.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">PasswordRequired</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a flag to indicate whether a password is required.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">Picture</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the picture of the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">PostalAddresses</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the array of end-user post office addresses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">PostalCodes</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the array of postal codes for the Postal Addresses. In Active Directory the array has a single element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">Profile</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the end-user's profile path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">RequireUniquePassword</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a flag to indicate whether  a new password must be different from ones in the password history list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">Schema</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the ADsPath string to the schema class object for this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">SeeAlso</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the array of ADsPaths of other objects related to this user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">TelephoneHome</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the list of home phone numbers of the user. In Active Directory the list has a single element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">TelephoneMobile</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the list of mobile phone numbers of the user. In Active Directory the list has a single element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">TelephoneNumber</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the list of work-related phone numbers. In Active Directory the list has a single element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">TelephonePager</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the list of pager phone numbers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">Title</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the user's title within the organization.

</td>
</tr>
</table> 


## -remarks



As with any other ADSI object, the container object creates a Windows user account object. First, bind to a container object. Then, call the  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadscontainer-create">IADsContainer::Create</a> method and specify mandatory or optional attributes.

With WinNT, you do not have to specify any additional attributes when creating a user. You may call the <a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadscontainer-create">IADsContainer::Create</a> method to create the user object directly.


```vb
Dim dom As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup

Set dom = GetObject("WinNT://MyDomain")
Set usr = dom.Create("user","jeffsmith")
usr.SetInfo

Cleanup:
    If(Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set mach = Nothing
    Set usr = Nothing

```


In this case, a domain user is created with the following default values.

<table>
<tr>
<th>Property</th>
<th>Value</th>
</tr>
<tr>
<td>
<b>Full Name</b>

</td>
<td>
SAM Account Name (such as jeffsmith)

</td>
</tr>
<tr>
<td>
<b>Password</b>

</td>
<td>
Empty

</td>
</tr>
<tr>
<td>
<b>User Must Change Password</b>

</td>
<td>
<b>TRUE</b>

</td>
</tr>
<tr>
<td>
<b>User Cannot Change Password</b>

</td>
<td>
<b>FALSE</b>

</td>
</tr>
<tr>
<td>
<b>Password Never Expires</b>

</td>
<td>
<b>FALSE</b>

</td>
</tr>
<tr>
<td>
<b>Account Disabled</b>

</td>
<td>
<b>FALSE</b>

</td>
</tr>
<tr>
<td>
<b>Group</b>

</td>
<td>
Domain User

</td>
</tr>
<tr>
<td>
<b>Profile</b>

</td>
<td>
Empty

</td>
</tr>
<tr>
<td>
<b>Account Never Expires</b>

</td>
<td>
<b>TRUE</b>

</td>
</tr>
</table>
 

To create a local user, bind to a target computer, as shown in the following code example.


```vb
Dim mach As IADsContainer
Dim usr as IADsUser

On Error GoTo Cleanup
Set mach = GetObject("WinNT://MyMachine,Computer")
Set usr = mach.Create("user","jeffsmith")
usr.SetInfo

Cleanup:
    If(Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set mach = Nothing
    Set usr = Nothing

```


The newly created local user will have the same default properties as the domain user. The group membership, however, will be "users", instead of "domain user".




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadscontainer-create">IADsContainer::Create</a>



<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsuser-property-methods">IADsUser
    Property Methods</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

