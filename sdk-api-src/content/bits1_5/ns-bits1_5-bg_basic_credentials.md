---
UID: NS:bits1_5.__MIDL_IBackgroundCopyJob2_0001
title: BG_BASIC_CREDENTIALS
description: The BG_BASIC_CREDENTIALS structure identifies the user name and password to authenticate.
helpviewer_keywords: ["*PBG_BASIC_CREDENTIALS","BG_BASIC_CREDENTIALS","BG_BASIC_CREDENTIALS structure [BITS]","_drz_bg_basic_credentials","bits.bg_basic_credentials","bits1_5/BG_BASIC_CREDENTIALS"]
old-location: bits\bg_basic_credentials.htm
tech.root: Bits
ms.assetid: e078e464-37b7-45ce-add8-6472a4607ff3
ms.date: 02/22/2019
ms.keywords: '*PBG_BASIC_CREDENTIALS, BG_BASIC_CREDENTIALS, BG_BASIC_CREDENTIALS structure [BITS], _drz_bg_basic_credentials, bits.bg_basic_credentials, bits1_5/BG_BASIC_CREDENTIALS'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BG_BASIC_CREDENTIALS
req.redist: BITS 1.5 on  Windows XP
f1_keywords:
 - __MIDL_IBackgroundCopyJob2_0001
 - bits1_5/__MIDL_IBackgroundCopyJob2_0001
 - BG_BASIC_CREDENTIALS
 - bits1_5/BG_BASIC_CREDENTIALS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits1_5.h
api_name:
 - BG_BASIC_CREDENTIALS
---

# BG_BASIC_CREDENTIALS structure


## -description

Identifies the user name and password to authenticate.

## -struct-fields

### -field UserName

A null-terminated string that contains the user name to authenticate. The user name is limited to 300 characters, not including the null terminator. The format of the user name depends on the authentication scheme requested. For example, for Basic, NTLM, and Negotiate authentication, the user name is of the form <em>DomainName</em><strong>\\</strong><em>UserName</em>. For Passport authentication, the user name is an email address. For more information, see Remarks.

If <strong>NULL</strong>, default credentials for this session context are used.

### -field Password

A null-terminated string that contains the password in plaintext. The password is limited to 65536 characters, not including the null terminator. The password can be blank. Set it to <strong>NULL</strong> if <strong>UserName</strong> is <strong>NULL</strong>. BITS encrypts the password before persisting the job if a network disconnect occurs or the user logs off.

Live ID encoded passwords are supported through Negotiate 2. For more information about Live IDs, see the <a href="/office/">Windows Live ID SDK</a>.

## -remarks

The following list identifies when the <b>UserName</b> and <b>Password</b> members are required based on the authentication scheme requested:

To protect the user name and password information, call the <b>SecureZeroMemory</b> function, defined in Winbase.h, to clear the <b>UserName</b> and <b>Password</b> buffers after you use the structure.

You can specify the user name like this.

<ul>
<li><i>DomainName</i><b>\</b><i>UserName</i>. Use <i>DomainName</i><b>\</b><i>UserName</i> if the server is in a domain and the <i>DomainName</i> is the domain to which the server belongs or is a trusted domain.

</li>
<li><i>ServerName</i><b>\</b><i>UserName</i>. Use <i>ServerName</i><b>\</b><i>UserName</i> if the account is a local account on the server. The <i>ServerName</i> is the name of the computer that is authenticating the credentials.

</li>
<li><i>UserName</i>. If you specify only <i>UserName</i>, the user's default domain name is prefixed to the user's name and the rules for the <i>DomainName</i><b>\</b><i>UserName</i> form apply.  Use this option only if the user is a member of a domain.

</li>
<li><b>NULL</b>. To use the user's logon credentials for NTLM or Kerberos authentication, set <b>UserName</b> to <b>NULL</b>. This works only if the user is in a trusted domain. Setting <b>UserName</b> to <b>NULL</b> for services running as a system account passes the computer's credentials for authentication. This option works only if the domain enables Kerberos authentication and you select Negotiate as the authentication scheme.

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials_union">BG_AUTH_CREDENTIALS_UNION</a>