---
UID: NF:wincred.CredUIParseUserNameW
title: CredUIParseUserNameW function (wincred.h)
description: The CredUIParseUserName function extracts the domain and user account name from a fully qualified user name. (Unicode)
helpviewer_keywords: ["CredUIParseUserName", "CredUIParseUserName function [Security]", "CredUIParseUserNameW", "_cred_creduiparseusername", "security.creduiparseusername", "wincred/CredUIParseUserName", "wincred/CredUIParseUserNameW"]
old-location: security\creduiparseusername.htm
tech.root: security
ms.assetid: 4a7fb207-f940-4610-a740-7bf5d58fb285
ms.date: 12/05/2018
ms.keywords: CredUIParseUserName, CredUIParseUserName function [Security], CredUIParseUserNameA, CredUIParseUserNameW, _cred_creduiparseusername, security.creduiparseusername, wincred/CredUIParseUserName, wincred/CredUIParseUserNameA, wincred/CredUIParseUserNameW
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredUIParseUserNameW (Unicode) and CredUIParseUserNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Credui.lib
req.dll: Credui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CredUIParseUserNameW
 - wincred/CredUIParseUserNameW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Credui.dll
 - Ext-MS-Win-security-credui-l1-1-1.dll
 - AnalogCredUI.dll
api_name:
 - CredUIParseUserName
 - CredUIParseUserNameA
 - CredUIParseUserNameW
---

# CredUIParseUserNameW function


## -description

The <b>CredUIParseUserName</b> function extracts the domain and user account name from a fully qualified user name.

## -parameters

### -param UserName [in]

Pointer to a <b>null</b>-terminated string that contains the user name to be parsed. The name must be in UPN or down-level format, or a certificate. Typically, <i>UserName</i> is received from the 
<a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsw">CredUIPromptForCredentials</a> or 
<a href="/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsw">CredUICmdLinePromptForCredentials</a>.

### -param user [out]

Pointer to a <b>null</b>-terminated string that receives the user account name.

### -param userBufferSize [in]

Maximum number of characters to write to the <i>pszUser</i> string including the terminating <b>null</b> character. 




<div class="alert"><b>Note</b>  CREDUI_MAX_USERNAME_LENGTH does NOT include the terminating <b>null</b> character.</div>
<div> </div>

### -param domain [out]

Pointer to a <b>null</b>-terminated string that receives the domain name. If <i>pszUserName</i> specifies a certificate, <i>pszDomain</i> will be <b>NULL</b>.

### -param domainBufferSize [in]

Maximum number of characters to write to the <i>pszDomain</i> string including the terminating <b>null</b> character. 




<div class="alert"><b>Note</b>  CREDUI_MAX_DOMAIN_TARGET_LENGTH does NOT include the terminating <b>null</b> character.</div>
<div> </div>

### -param userName [in]

Pointer to a <b>null</b>-terminated string that contains the user name to be parsed. The name must be in UPN or down-level format, or a certificate. Typically, <i>pszUserName</i> is received from the 
<a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa">CredUIPromptForCredentials</a> or 
<a href="/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa">CredUICmdLinePromptForCredentials</a>.

## -returns

This function returns the following:

<ul>
<li>NO_ERROR 


The user name is valid.

</li>
<li>ERROR_INVALID_ACCOUNT_NAME 


The user name is not valid.

</li>
<li>ERROR_INSUFFICIENT_BUFFER 


One of the buffers is too small.

</li>
<li>ERROR_INVALID_PARAMETER 


<ul>
<li><i>ulUserMaxChars</i> or <i>ulDomainMaxChars</i> is zero.</li>
<li><i>pszUserName</i>, <i>pszUser</i>, or <i>pszDomain</i> is <b>NULL</b>.</li>
</ul>
</li>
</ul>

## -remarks

This function parses the user name information returned by the 
<a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa">CredUIPromptForCredentials</a> and 
<a href="/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa">CredUICmdLinePromptForCredentials</a> functions so that the resulting credentials can be passed to functions, such as <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a>, that require the user name and domain as separate strings.

The following formats are supported:

<ul>
<li>&lt;MarshalledCredentialReference&gt; 


Marshaled credential reference as defined by 
<a href="/windows/desktop/api/wincred/nf-wincred-credismarshaledcredentiala">CredIsMarshaledCredential</a>. Such a credential is returned in the <i>User</i> parameter. The <i>Domain</i> parameter is set to an empty string.

</li>
<li>&lt;DomainName&gt;\&lt;UserName&gt; 


&lt;UserName&gt; is returned in the <i>User</i> parameter and the &lt;DomainName&gt; is returned is the <i>Domain</i> parameter. The name is considered to have this syntax if the <i>UserName</i> contains a backslash (\\).

</li>
<li>&lt;UserName&gt;@&lt;DNSDomainName&gt; 


The entire string is returned in the <i>User</i> parameter. The <i>Domain</i> parameter is set to an empty string. For this syntax, the last @ in the string is used because &lt;UserName&gt; can contain an @ but &lt;DNSDomainName&gt; cannot.

</li>
</ul>




> [!NOTE]
> The wincred.h header defines CredUIParseUserName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wincred/nf-wincred-credismarshaledcredentiala">CredIsMarshaledCredential</a>



<a href="/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa">CredUICmdLinePromptForCredentials</a>



<a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa">CredUIPromptForCredentials</a>



<a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a>
