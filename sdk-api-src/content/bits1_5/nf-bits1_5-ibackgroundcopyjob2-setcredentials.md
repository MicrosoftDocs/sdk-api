---
UID: NF:bits1_5.IBackgroundCopyJob2.SetCredentials
title: IBackgroundCopyJob2::SetCredentials
description: Specifies the credentials to use for a proxy or remote server user authentication request.
helpviewer_keywords: ["IBackgroundCopyJob2 interface [BITS]","SetCredentials method","IBackgroundCopyJob2.SetCredentials","IBackgroundCopyJob2::SetCredentials","SetCredentials","SetCredentials method [BITS]","SetCredentials method [BITS]","IBackgroundCopyJob2 interface","_drz_ibackgroundcopyjob2_setcredentials","bits.ibackgroundcopyjob2_setcredentials","bits1_5/IBackgroundCopyJob2::SetCredentials"]
old-location: bits\ibackgroundcopyjob2_setcredentials.htm
tech.root: Bits
ms.assetid: adaffc21-7df1-48ca-8e05-bdb09663a49b
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob2 interface [BITS],SetCredentials method, IBackgroundCopyJob2.SetCredentials, IBackgroundCopyJob2::SetCredentials, SetCredentials, SetCredentials method [BITS], SetCredentials method [BITS],IBackgroundCopyJob2 interface, _drz_ibackgroundcopyjob2_setcredentials, bits.ibackgroundcopyjob2_setcredentials, bits1_5/IBackgroundCopyJob2::SetCredentials
req.header: bits1_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits1_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: BitsPrx2.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: BITS 1.5 on  Windows XP
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob2::SetCredentials
 - bits1_5/IBackgroundCopyJob2::SetCredentials
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx2.dll
api_name:
 - IBackgroundCopyJob2.SetCredentials
---

# IBackgroundCopyJob2::SetCredentials


## -description

Specifies the credentials to use for a proxy or remote server user authentication request.

## -parameters

### -param credentials [in]

Identifies the target (proxy or server), authentication scheme, and the user's credentials to use for user authentication. For details, see the 
<a href="/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials">BG_AUTH_CREDENTIALS</a> structure.

## -returns

This method returns the following return values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_AUTH_TARGET</b></dt>
</dl>
</td>
<td width="60%">
Unrecognized target enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_AUTH_SCHEME</b></dt>
</dl>
</td>
<td width="60%">
Unrecognized scheme enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_USERNAME_TOO_LARGE</b></dt>
</dl>
</td>
<td width="60%">
The user name is too long. For the limit, see the <a href="/windows/desktop/api/bits1_5/ns-bits1_5-bg_basic_credentials">BG_BASIC_CREDENTIALS</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_PASSWORD_TOO_LARGE</b></dt>
</dl>
</td>
<td width="60%">
The password is too long. For the limit, see the <a href="/windows/desktop/api/bits1_5/ns-bits1_5-bg_basic_credentials">BG_BASIC_CREDENTIALS</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The UserName and Password members of the <a href="/windows/desktop/api/bits1_5/ns-bits1_5-bg_basic_credentials">BG_BASIC_CREDENTIALS</a> structure cannot be <b>NULL</b> if you specify the Basic or Digest scheme.

</td>
</tr>
</table>

## -remarks

 BITS provides the credentials to a proxy or server in response to a request for user authentication. Set the credentials before the initial call to <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume">Resume</a>. 

You must call this method for each target and scheme pair that you want to provide. For example, if you want to specify proxy credentials for both Basic and Digest authentication, you would call this method once to specify the Basic credentials and a second time to specify the Digest credentials.

If the job currently contains credentials with the same target and scheme pair, the existing credentials are replaced with the new credentials. The credentials persist for the life of the job. To remove the credentials from the job, call the 
<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-removecredentials">IBackgroundCopyJob2::RemoveCredentials</a> method.

If you know the schemes the proxy or server will request, you can provide only those credentials. Otherwise, provide credentials for all schemes. 

The job enters the <b>BG_JOB_STATE_ERROR</b> state if you do not provide the credentials requested by the proxy or server, or the proxy or server cannot authenticate the credentials. Check the error code to determine if the authentication failed at the server (<b>BG_E_HTTP_ERROR_401</b>) or proxy (<b>BG_E_HTTP_ERROR_407</b>). To retrieve the error code, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-geterror">IBackgroundCopyJob::GetError</a> method to retrieve an 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyerror">IBackgroundCopyError</a> interface pointer. Then, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-geterror">IBackgroundCopyError::GetError</a> method to retrieve the error code. After you determine where the authentication failed (proxy or server), specify new credentials to use for the proxy or server and call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume">IBackgroundCopyJob::Resume</a> method to resume the job. Because you cannot determine which scheme failed, specify credentials for all schemes before calling the 
<b>Resume</b> method.

There is no method to retrieve credentials that you have set.

You must call this method in the context of the job's owner.

Calling the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-takeownership">IBackgroundCopyJob::TakeOwnership</a> method removes the credentials from the job.

To specify implicit credentials (the logged on user's credentials), set the scheme to NTLM and the user name and password to <b>NULL</b>. If you specify implicit credentials for a proxy, BITS will also use the implicit credentials for server authentication unless you specify explicit server credentials. 

<div class="alert"><b>Note</b>  BITS ignores credentials for <a href="/windows/desktop/api/bits/ns-bits-bg_file_info">remote names</a> that specify an SMB path.</div>
<div> </div>
<div class="alert"><b>Note</b>  BITS does not authenticate the server or encrypt the channel. Use HTTPS if this is an issue for your application.</div>
<div> </div>

#### Examples

The following example shows how to call the 
<b>SetCredentials</b> method to specify Basic credentials for a server user authentication request. The example uses the 
<a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa">CredUIPromptForCredentials</a> function to capture the user name and password. The example assumes a valid 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a> interface pointer, pJob. The example uses the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function to clear the memory locations associated with the sensitive information. The <b>SecureZeroMemory</b> function is defined in WinBase.h.


```cpp
#define MAX_STR_LENGTH 300+1    // BITS limit for user name and password

CREDUI_INFO cuiinfo;
WCHAR szUserName[MAX_STR_LENGTH];  
WCHAR szPassword[MAX_STR_LENGTH];
DWORD rc;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
BG_AUTH_CREDENTIALS ac;

cuiinfo.cbSize = sizeof(CREDUI_INFO);
cuiinfo.hbmBanner = NULL;
cuiinfo.hwndParent = NULL; //Desktop is parent
cuiinfo.pszCaptionText = L"Server Authentication";
cuiinfo.pszMessageText = L"Enter user credentials for Basic authentication.";

//Initialize the UserName and Password fields. This example sets  
//UserName to blank, but you could also set UserName to the owner 
//of the job or the current user. For an example that retrieves the owner's
//name, see the example code for the IBackgroundCopyJob::GetOwner method. 
szUserName[0] = L'\0';
szPassword[0] = L'\0';
rc = CredUIPromptForCredentials(&cuiinfo, NULL, NULL, 0,
    szUserName, MAX_STR_LENGTH,
    szPassword, MAX_STR_LENGTH, 
    NULL, CREDUI_FLAGS_DO_NOT_PERSIST | CREDUI_FLAGS_GENERIC_CREDENTIALS);

if (NO_ERROR == rc)
{
    pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
    ac.Target = BG_AUTH_TARGET_SERVER;
    ac.Scheme = BG_AUTH_SCHEME_BASIC;
    ac.Credentials.Basic.UserName = szUserName;
    ac.Credentials.Basic.Password = szPassword;
    hr = pJob2->SetCredentials(&ac);
    if (FAILED(hr))
    {
      //Handle error
    }
    SecureZeroMemory(szUserName, sizeof(szUserName));
    SecureZeroMemory(szPassword, sizeof(szPassword));
}
```

## -see-also

<a href="/windows/desktop/Bits/authentication">Authentication</a>



<a href="/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials">BG_AUTH_CREDENTIALS</a>



<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-removecredentials">IBackgroundCopyJob2::RemoveCredentials</a>