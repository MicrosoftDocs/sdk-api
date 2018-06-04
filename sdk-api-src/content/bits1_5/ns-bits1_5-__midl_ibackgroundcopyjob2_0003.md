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

# __MIDL_IBackgroundCopyJob2_0003 structure


## -description


The 
<b>BG_BASIC_CREDENTIALS</b> structure identifies the user name and password to authenticate.


## -struct-fields




### -field UserName

Null-terminated string that contains the user name to authenticate. The user name is limited to 300 characters, not including the null terminator. The format of the user name depends on the authentication scheme requested. For example, for Basic, NTLM, and Negotiate authentication, the user name is of the form <i>DomainName</i><b>\</b><i>UserName</i>. For Passport authentication, the user name is an email address. For more information, see Remarks.

If <b>NULL</b>, default credentials for this session context are used.


### -field Password

Null-terminated string that contains the password in plaintext. The password is limited to 65536 characters, not including the null terminator. The password can be blank. Set it to <b>NULL</b> if <b>UserName</b> is <b>NULL</b>. BITS encrypts the password before persisting the job if a network disconnect occurs or the user logs off.

Live ID encoded passwords are supported through Negotiate 2. For more information about Live IDs, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=147129">Windows Live ID SDK</a>.   


## -remarks



The following list identifies when the <b>UserName</b> and <b>Password</b> members are required based on the authentication scheme requested:



To protect the user name and password information, call the <b>SecureZeroMemory</b> function, defined in Winbase.h, to clear the <b>UserName</b> and <b>Password</b> buffers after you use the structure.

You can specify the user name as:

<ul>
<li><i>DomainName</i><b>\</b><i>UserName</i>Use <i>DomainName</i><b>\</b><i>UserName</i> if the server is in a domain and the <i>DomainName</i> is the domain to which the server belongs or is a trusted domain.

</li>
<li><i>ServerName</i><b>\</b><i>UserName</i>Use <i>ServerName</i><b>\</b><i>UserName</i> if the account is a local account on the server. The <i>ServerName</i> is the name of the computer that is authenticating the credentials.

</li>
<li><i>UserName</i>If you specify only <i>UserName</i>, the user's default domain name is prefixed to the user's name and the rules for the <i>DomainName</i><b>\</b><i>UserName</i> form apply.  Use this option only if the user is a member of a domain.

</li>
<li><b>NULL</b>To use the user's logon credentials for NTLM or Kerberos authentication, set <b>UserName</b> to <b>NULL</b>. This works only if the user is in a trusted domain. Setting <b>UserName</b> to <b>NULL</b> for services running as a system account passes the computer's credentials for authentication. This option works only if the domain enables Kerberos authentication and you select Negotiate as the authentication scheme.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/c16c616c-f4cb-483d-8a15-6ff9d45762ae">BG_AUTH_CREDENTIALS_UNION</a>
 

 

