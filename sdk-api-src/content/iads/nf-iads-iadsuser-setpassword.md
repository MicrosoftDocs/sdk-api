---
UID: NF:iads.IADsUser.SetPassword
title: IADsUser::SetPassword (iads.h)
description: Sets the user password to a specified value.
helpviewer_keywords: ["IADsUser interface [ADSI]","SetPassword method","IADsUser.SetPassword","IADsUser::SetPassword","SetPassword","SetPassword method [ADSI]","SetPassword method [ADSI]","IADsUser interface","_ds_iadsuser_setpassword","adsi.iadsuser__setpassword","adsi.iadsuser_setpassword","iads/IADsUser::SetPassword"]
old-location: adsi\iadsuser_setpassword.htm
tech.root: adsi
ms.assetid: cad38632-9f0a-4707-9086-b1248d6f31a6
ms.date: 12/05/2018
ms.keywords: IADsUser interface [ADSI],SetPassword method, IADsUser.SetPassword, IADsUser::SetPassword, SetPassword, SetPassword method [ADSI], SetPassword method [ADSI],IADsUser interface, _ds_iadsuser_setpassword, adsi.iadsuser__setpassword, adsi.iadsuser_setpassword, iads/IADsUser::SetPassword
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
 - IADsUser::SetPassword
 - iads/IADsUser::SetPassword
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
 - IADsUser.SetPassword
---

## -description

The <b>IADsUser::SetPassword</b> method sets the user password to a specified value. For the LDAP provider, the user account must have been created and stored in the underlying directory using  <a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a> before <b>IADsUser::SetPassword</b> is called.

The WinNT provider, however, enables you to set the password on a newly created user object prior to calling <a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">SetInfo</a>. This ensures that you create  passwords that comply with the system password policy before you create the user account.

## -parameters

### -param NewPassword

A <b>BSTR</b> that contains the new password.

## -returns

This method supports the standard return values, including <b>S_OK</b>. For other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The LDAP provider for Active Directory uses one of three processes to set the password; third-party LDAP directories such as iPlanet do not use this password authentication process. The method may vary according to the network configuration. Attempts to set the password occur in the following order:

<ul>
<li>First, the LDAP provider attempts to use LDAP over a 128-bit SSL connection. For LDAP SSL to operate successfully, the LDAP server must have the appropriate server authentication certificate installed and the clients running the ADSI code must trust the authority that issued those certificates. Both the server and the client must support 128-bit encryption.</li>
<li>Second, if the SSL connection is unsuccessful, the LDAP provider attempts to use Kerberos.</li>
<li>Third, if Kerberos is unsuccessful, the LDAP provider attempts a <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> API call. In previous releases, ADSI called <b>NetUserSetInfo</b> in the security context in which the thread was running, and not the security context specified in the call to <a href="/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject">IADsOpenDSObject::OpenDSObject</a> or <a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a>. In later releases, this was changed so that the ADSI LDAP provider would impersonate the user specified in the <b>OpenDSObject</b> call when it calls NetUserSetInfo.</li>
</ul>
In Active Directory, the caller must have the <a href="/windows/desktop/ADSchema/r-user-force-change-password">Reset Password</a> extended control access right to set the password with this method.


#### Examples

The following code example shows how to set the user password, if you have the permission to do so.


```vb
Dim usr As IADsUser
Dim szPassword As String
On Error GoTo Cleanup

' Add code to securely get the password.

Set usr = GetObject("LDAP://MyLdapSvr/CN=JeffSmith,DC=Fabrikam")
usr.SetPassword szPassword

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```


The following code example shows how to set the user password, if you have the permission to do so.


```cpp
HRESULT SetPassword(IADsUser *pUser, BSTR password)
{
    HRESULT hr=S_OK;
    if(!pUser) { return E_FAIL;}
    hr = pUser->SetPassword(password);
    if (hr == S_OK) printf("User password has been set");
    pUser->Release();
    return hr;
}

```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsmembers">IADsMembers</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsserviceoperations">IADsServiceOperations</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsuser">IADsUser</a>



<a href="/windows/desktop/ADSI/iadsuser-property-methods">IADsUser
  Property Methods</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>