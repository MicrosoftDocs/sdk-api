---
UID: NF:iads.IADsUser.SetPassword
title: IADsUser::SetPassword
author: windows-sdk-content
description: Sets the user password to a specified value.
old-location: adsi\iadsuser_setpassword.htm
tech.root: adsi
ms.assetid: cad38632-9f0a-4707-9086-b1248d6f31a6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IADsUser interface [ADSI],SetPassword method, IADsUser.SetPassword, IADsUser::SetPassword, SetPassword, SetPassword method [ADSI], SetPassword method [ADSI],IADsUser interface, _ds_iadsuser_setpassword, adsi.iadsuser__setpassword, adsi.iadsuser_setpassword, iads/IADsUser::SetPassword
ms.topic: method
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
 - IADsUser.SetPassword
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsUser::SetPassword


## -description



   The <b>IADsUser::SetPassword</b> method sets the user password to a specified value. For the LDAP provider, the user account must have been created and stored in the underlying directory using  <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a> before <b>IADsUser::SetPassword</b> is called.

The WinNT provider, however, enables you to set the password on a newly created user object prior to calling <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">SetInfo</a>. This ensures that you create  passwords that comply with the system password policy before you create the user account.


## -parameters




### -param NewPassword

TBD




#### - bstrNewPassword [in]

A <b>BSTR</b> that contains the new password.


## -returns



This method supports the standard return values, including <b>S_OK</b>. For other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The LDAP provider for Active Directory uses one of three processes to set the password; third-party LDAP directories such as iPlanet do not use this password authentication process. The method may vary according to the network configuration. Attempts to set the password occur in the following order:

<ul>
<li>First, the LDAP provider attempts to use LDAP over a 128-bit SSL connection. For LDAP SSL to operate successfully, the LDAP server must have the appropriate server authentication certificate installed and the clients running the ADSI code must trust the authority that issued those certificates. Both the server and the client must support 128-bit encryption.</li>
<li>Second, if the SSL connection is unsuccessful, the LDAP provider attempts to use Kerberos.</li>
<li>Third, if Kerberos is unsuccessful, the LDAP provider attempts a <a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> API call. In previous releases, ADSI called <b>NetUserSetInfo</b> in the security context in which the thread was running, and not the security context specified in the call to <a href="https://msdn.microsoft.com/9984ddb4-58bb-4264-930b-07e6534dc69f">IADsOpenDSObject::OpenDSObject</a> or <a href="https://msdn.microsoft.com/c4b85d8e-b33b-47a4-b7d7-5f901f80dce9">ADsOpenObject</a>. In later releases, this was changed so that the ADSI LDAP provider would impersonate the user specified in the <b>OpenDSObject</b> call when it calls NetUserSetInfo.</li>
</ul>
In Active Directory, the caller must have the <a href="https://msdn.microsoft.com/7bf078f4-b123-45dc-9468-ffe35a46c32c">Reset Password</a> extended control access right to set the password with this method.


#### Examples

The following code example shows how to set the user password, if you have the permission to do so.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim usr As IADsUser
Dim szPassword As String
On Error GoTo Cleanup

' Add code to securely get the password.

Set usr = GetObject("LDAP://MyLdapSvr/CN=JeffSmith,DC=Fabrikam")
usr.SetPassword szPassword

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set usr = Nothing</pre>
</td>
</tr>
</table></span></div>
The following code example shows how to set the user password, if you have the permission to do so.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT SetPassword(IADsUser *pUser, BSTR password)
{
    HRESULT hr=S_OK;
    if(!pUser) { return E_FAIL;}
    hr = pUser-&gt;SetPassword(password);
    if (hr == S_OK) printf("User password has been set");
    pUser-&gt;Release();
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a>



<a href="https://msdn.microsoft.com/889e8fc1-61a6-4a3a-82ac-85d41f664149">IADsMembers</a>



<a href="https://msdn.microsoft.com/f2459ca2-8a14-4343-bec6-ef3775dbf415">IADsServiceOperations</a>



<a href="https://msdn.microsoft.com/6eea74c2-2d6d-4dfd-9a22-3da2d5ce49bf">IADsUser</a>



<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">IADsUser
  Property Methods</a>



<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a>
 

 

