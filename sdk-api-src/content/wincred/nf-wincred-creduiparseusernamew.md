---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CredUIParseUserNameW function


## -description



			The <b>CredUIParseUserName</b> function extracts the domain and user account name from a fully qualified user name.


## -parameters




### -param UserName

TBD


### -param user

TBD


### -param userBufferSize

TBD


### -param domain

TBD


### -param domainBufferSize

TBD




#### - pszDomain [out]

Pointer to a <b>null</b>-terminated string that receives the domain name. If <i>pszUserName</i> specifies a certificate, <i>pszDomain</i> will be <b>NULL</b>.


#### - pszUser [out]

Pointer to a <b>null</b>-terminated string that receives the user account name.


#### - pszUserName [in]

Pointer to a <b>null</b>-terminated string that contains the user name to be parsed. The name must be in UPN or down-level format, or a certificate. Typically, <i>pszUserName</i> is received from the 
<a href="https://msdn.microsoft.com/97a8e750-3e63-4e6f-a875-1e5c49c30dd4">CredUIPromptForCredentials</a> or 
<a href="https://msdn.microsoft.com/5b5bfe87-8f31-4228-931e-50cfc399b66b">CredUICmdLinePromptForCredentials</a>.


#### - ulDomainMaxChars [in]

Maximum number of characters to write to the <i>pszDomain</i> string including the terminating <b>null</b> character. 




<div class="alert"><b>Note</b>  CREDUI_MAX_DOMAIN_TARGET_LENGTH does NOT include the terminating <b>null</b> character.</div>
<div> </div>

#### - ulUserMaxChars [in]

Maximum number of characters to write to the <i>pszUser</i> string including the terminating <b>null</b> character. 




<div class="alert"><b>Note</b>  CREDUI_MAX_USERNAME_LENGTH does NOT include the terminating <b>null</b> character.</div>
<div> </div>

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
<a href="https://msdn.microsoft.com/97a8e750-3e63-4e6f-a875-1e5c49c30dd4">CredUIPromptForCredentials</a> and 
<a href="https://msdn.microsoft.com/5b5bfe87-8f31-4228-931e-50cfc399b66b">CredUICmdLinePromptForCredentials</a> functions so that the resulting credentials can be passed to functions, such as <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a>, that require the user name and domain as separate strings.

The following formats are supported:

<ul>
<li>&lt;MarshalledCredentialReference&gt; 


Marshaled credential reference as defined by 
<a href="https://msdn.microsoft.com/fc902c0c-41e0-4178-8ca0-227a1d218388">CredIsMarshaledCredential</a>. Such a credential is returned in the <i>User</i> parameter. The <i>Domain</i> parameter is set to an empty string.

</li>
<li>&lt;DomainName&gt;\&lt;UserName&gt; 


&lt;UserName&gt; is returned in the <i>User</i> parameter and the &lt;DomainName&gt; is returned is the <i>Domain</i> parameter. The name is considered to have this syntax if the <i>UserName</i> contains a backslash (\).

</li>
<li>&lt;UserName&gt;@&lt;DNSDomainName&gt; 


The entire string is returned in the <i>User</i> parameter. The <i>Domain</i> parameter is set to an empty string. For this syntax, the last @ in the string is used because &lt;UserName&gt; can contain an @ but &lt;DNSDomainName&gt; cannot.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/fc902c0c-41e0-4178-8ca0-227a1d218388">CredIsMarshaledCredential</a>



<a href="https://msdn.microsoft.com/5b5bfe87-8f31-4228-931e-50cfc399b66b">CredUICmdLinePromptForCredentials</a>



<a href="https://msdn.microsoft.com/97a8e750-3e63-4e6f-a875-1e5c49c30dd4">CredUIPromptForCredentials</a>



<a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a>
 

 

