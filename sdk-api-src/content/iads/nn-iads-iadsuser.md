---
UID: NN:iads.IADsUser
title: IADsUser (iads.h)
description: The IADsUser interface is a dual interface that inherits from IADs.
helpviewer_keywords: ["IADsUser","IADsUser interface [ADSI]","IADsUser interface [ADSI]","described","_ds_iadsuser","adsi.iadsuser","iads/IADsUser"]
old-location: adsi\iadsuser.htm
tech.root: adsi
ms.assetid: 6eea74c2-2d6d-4dfd-9a22-3da2d5ce49bf
ms.date: 12/05/2018
ms.keywords: IADsUser, IADsUser interface [ADSI], IADsUser interface [ADSI],described, _ds_iadsuser, adsi.iadsuser, iads/IADsUser
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsUser
 - iads/IADsUser
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsUser
---

# IADsUser interface


## -description

The <b>IADsUser</b> interface is a dual interface that inherits from  <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is designed to represent and manage an end-user account on a network. Call the methods of this interface to access and manipulate end-user account data. Such data includes names of the user, telephone numbers, job title, and so on. This interface supports features for determining the group association of the user, and for setting or changing the password.
   

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

The <b>IADsUser</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsUser</b> also has these types of members:

## -remarks

As with any other ADSI object, the container object creates a Windows user account object. First, bind to a container object. Then, call the  <a href="/windows/desktop/api/iads/nf-iads-iadscontainer-create">IADsContainer::Create</a> method and specify mandatory or optional attributes.

With WinNT, you do not have to specify any additional attributes when creating a user. You may call the <a href="/windows/desktop/api/iads/nf-iads-iadscontainer-create">IADsContainer::Create</a> method to create the user object directly.


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

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/iads/nf-iads-iadscontainer-create">IADsContainer::Create</a>



<a href="/windows/desktop/ADSI/iadsuser-property-methods">IADsUser
    Property Methods</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
