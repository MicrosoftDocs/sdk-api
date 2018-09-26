---
UID: NN:iads.IADsUser
title: IADsUser
author: windows-sdk-content
description: The IADsUser interface is a dual interface that inherits from IADs.
old-location: adsi\iadsuser.htm
tech.root: ADSI
ms.assetid: 6eea74c2-2d6d-4dfd-9a22-3da2d5ce49bf
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IADsUser, IADsUser interface [ADSI], IADsUser interface [ADSI],described, _ds_iadsuser, adsi.iadsuser, iads/IADsUser
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsUser interface


## -description


The <b>IADsUser</b> interface is a dual interface that inherits from  <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>. It is designed to represent and manage an end-user account on a network. Call the methods of this interface to access and manipulate end-user account data. Such data includes names of the user, telephone numbers, job title, and so on. This interface supports features for determining the group association of the user, and for setting or changing the password.
   

To bind to a domain user through a WinNT provider, use the domain name as part of the ADsPath, as shown in the following code example.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>GetObject("WinNT://MYDOMAIN/jeffsmith,user")</pre>
</td>
</tr>
</table></span></div>Similarly, use the computer name as part of the ADsPath to bind to a local user.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>GetObject("WinNT://MYCOMPUTER/jeffsmith,user")</pre>
</td>
</tr>
</table></span></div>In Active Directory, domain users reside in the directory. The following code example shows how to bind to a domain user through an LDAP provider.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>GetObject("LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com")</pre>
</td>
</tr>
</table></span></div>However, local accounts reside in the local SAM database and the LDAP provider does not communicate with the local database. Thus, to bind to a local user, you must go through a WinNT provider as described in the second code example.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsUser</b> interface inherits from <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> and <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>. <b>IADsUser</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/279087b1-450a-4089-a5f6-257849ae583f">ChangePassword</a>
</td>
<td align="left" width="63%">
Changes password from the specified existing value to a new value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">Get</a>
</td>
<td align="left" width="63%">
Gets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cda6b8e7-fadc-4e0b-8217-66b37bf7efbd">GetEx</a>
</td>
<td align="left" width="63%">
Gets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">GetInfo</a>
</td>
<td align="left" width="63%">
Loads the property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/306ab953-890a-4ec9-8ec2-bea73888ea20">GetInfoEx</a>
</td>
<td align="left" width="63%">
Loads specific property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d250815-a7d8-4e61-b125-a66f1c2fde43">Groups</a>
</td>
<td align="left" width="63%">
Determines the groups to which this end-user belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">Put</a>
</td>
<td align="left" width="63%">
Sets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb9d9b2c-9efc-4462-ac4b-9a2fbf0b5ec7">PutEx</a>
</td>
<td align="left" width="63%">
Sets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">SetInfo</a>
</td>
<td align="left" width="63%">
Persists the changes on this object to the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cad38632-9f0a-4707-9086-b1248d6f31a6">SetPassword</a>
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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">AccountDisabled</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">AccountExpirationDate</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">AdsPath</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">BadLoginAddress</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">BadLoginCount</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Class</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">Department</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">Description</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">Division</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">EmailAddress</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">EmployeeID</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">FaxNumber</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">FirstName</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">FullName</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">GraceLoginsAllowed</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">GraceLoginsRemaining</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">GUID</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">HomeDirectory</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">HomePage</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">IsAccountLocked</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">Languages</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">LastFailedLogin</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">LastLogin</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">LastLogoff</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">LastName</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">LoginHours</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">LoginScript</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">LoginWorkstations</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">Manager</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">MaxLogins</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">MaxStorage</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Name</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">NamePrefix</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">NameSuffix</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">OfficeLocations</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">OtherName</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Parent</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">PasswordExpirationDate</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">PasswordLastChanged</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">PasswordMinimumLength</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">PasswordRequired</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">Picture</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">PostalAddresses</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">PostalCodes</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">Profile</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">RequireUniquePassword</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Schema</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">SeeAlso</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">TelephoneHome</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">TelephoneMobile</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">TelephoneNumber</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">TelephonePager</a>


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

<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">Title</a>


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



As with any other ADSI object, the container object creates a Windows user account object. First, bind to a container object. Then, call the  <a href="https://msdn.microsoft.com/9498ef4d-7a03-487f-91a7-189f17a38a24">IADsContainer::Create</a> method and specify mandatory or optional attributes.

With WinNT, you do not have to specify any additional attributes when creating a user. You may call the <a href="https://msdn.microsoft.com/9498ef4d-7a03-487f-91a7-189f17a38a24">IADsContainer::Create</a> method to create the user object directly.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim dom As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup

Set dom = GetObject("WinNT://MyDomain")
Set usr = dom.Create("user","jeffsmith")
usr.SetInfo

Cleanup:
    If(Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set mach = Nothing
    Set usr = Nothing
</pre>
</td>
</tr>
</table></span></div>
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

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim mach As IADsContainer
Dim usr as IADsUser

On Error GoTo Cleanup
Set mach = GetObject("WinNT://MyMachine,Computer")
Set usr = mach.Create("user","jeffsmith")
usr.SetInfo

Cleanup:
    If(Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set mach = Nothing
    Set usr = Nothing
</pre>
</td>
</tr>
</table></span></div>
The newly created local user will have the same default properties as the domain user. The group membership, however, will be "users", instead of "domain user".




## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/9498ef4d-7a03-487f-91a7-189f17a38a24">IADsContainer::Create</a>



<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">IADsUser
    Property Methods</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

