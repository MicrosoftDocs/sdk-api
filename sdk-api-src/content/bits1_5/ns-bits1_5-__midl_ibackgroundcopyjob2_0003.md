---
UID: NS:bits1_5.__MIDL_IBackgroundCopyJob2_0003
title: "__MIDL_IBackgroundCopyJob2_0003"
author: windows-sdk-content
description: The BG_BASIC_CREDENTIALS structure identifies the user name and password to authenticate.
old-location: bits\bg_basic_credentials.htm
old-project: bits
ms.assetid: e078e464-37b7-45ce-add8-6472a4607ff3
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PBG_BASIC_CREDENTIALS, BG_BASIC_CREDENTIALS, BG_BASIC_CREDENTIALS structure [BITS], __MIDL_IBackgroundCopyJob2_0003, _drz_bg_basic_credentials, bits.bg_basic_credentials, bits1_5/BG_BASIC_CREDENTIALS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: BG_BASIC_CREDENTIALS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits1_5.h
api_name:
 - BG_BASIC_CREDENTIALS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

