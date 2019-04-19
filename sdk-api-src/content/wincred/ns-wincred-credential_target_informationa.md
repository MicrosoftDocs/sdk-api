---
UID: NS:wincred._CREDENTIAL_TARGET_INFORMATIONA
title: CREDENTIAL_TARGET_INFORMATIONA (wincred.h)
author: windows-sdk-content
description: The CREDENTIAL_TARGET_INFORMATION structure contains the target computer's name, domain, and tree.
old-location: security\credential_target_information.htm
tech.root: SecAuthN
ms.assetid: 92180f2c-ef7c-4481-9b6f-19234c114afb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCREDENTIAL_TARGET_INFORMATIONA, CREDENTIAL_TARGET_INFORMATION, CREDENTIAL_TARGET_INFORMATION structure [Security], CREDENTIAL_TARGET_INFORMATIONA, PCREDENTIAL_TARGET_INFORMATION, PCREDENTIAL_TARGET_INFORMATION structure pointer [Security], _cred_credential_target_information, security.credential_target_information, wincred/CREDENTIAL_TARGET_INFORMATION, wincred/PCREDENTIAL_TARGET_INFORMATION"
ms.topic: struct
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinCred.h
api_name:
 - CREDENTIAL_TARGET_INFORMATION
product: Windows
targetos: Windows
req.typenames: CREDENTIAL_TARGET_INFORMATIONA, *PCREDENTIAL_TARGET_INFORMATIONA
req.redist: 
ms.custom: 19H1
---

# CREDENTIAL_TARGET_INFORMATIONA structure


## -description


The <b>CREDENTIAL_TARGET_INFORMATION</b> structure contains the target computer's name, domain, and tree.


## -struct-fields




### -field TargetName

Name of the target server as specified by the caller accessing the target. It is typically the NetBIOS or DNS name of the target server.


### -field NetbiosServerName

NetBIOS name of the target server. If the name is not known, this member can be <b>NULL</b>.


### -field DnsServerName

DNS name of the target server. If the name is not known, this member can be <b>NULL</b>.


### -field NetbiosDomainName

NetBIOS name of the target server's domain. If the name is not known, this member can be <b>NULL</b>. If the target server is a member of a workgroup, this member must be <b>NULL</b>.


### -field DnsDomainName

DNS name of the target server's domain. If the name is not known, this member can be <b>NULL</b>. If the target server is a member of a workgroup, this member must be <b>NULL</b>.


### -field DnsTreeName

DNS name of the target server's tree. If the tree name is not known, this member can be <b>NULL</b>. If the target server is a member of a workgroup, this member must be <b>NULL</b>.


### -field PackageName

Name of the authentication package that determined the values <b>NetbiosServerName</b>, <b>DnsServerName</b>, <b>NetbiosDomainName</b>, <b>DnsDomainName</b>, and <b>DnsTreeName</b> as a function of <b>TargetName</b>. This member can be passed to <a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle</a> as the package name.


### -field Flags

Attributes of the target. 




<ul>
<li>CRED_TI_SERVER_FORMAT_UNKNOWN 


(1) — Set if the authentication package cannot determine whether the server name is a DNS name or a NetBIOS name. In that case, the <b>NetbiosServerName</b> member is set to <b>NULL</b> and the <b>DnsServerName</b> member is set to the server name of unknown format.

</li>
<li>CRED_TI_DOMAIN_FORMAT_UNKNOWN 


(2) — Set if the authentication package cannot determine whether the domain name is a DNS name or a NetBIOS name. In that case, the <b>NetbiosDomainName</b> member is set to <b>NULL</b> and the <b>DnsDomainName</b> member is set to the domain name of unknown format.

</li>
<li>CRED_TI_ONLY_PASSWORD_REQUIRED 


(4) — Set if the authentication package has determined that the server only needs a password to authenticate. The caller can use this flag  to prompt only for a password and not a user name.

Stored credentials require a UserName member. A value of &lt;<i>DnsServerName</i>&gt;\Guest or &lt;<i>NetbiosServerName</i>&gt;\Guest should be used for these servers.

</li>
</ul>

### -field CredTypeCount

Number of elements in the <b>CredTypes</b> array.


### -field CredTypes

Array specifying the credential types acceptable by the authentication package used by the target server. Each element is one of the CRED_TYPE_* defines. The order of this array specifies the preference order of the authentication package. More preferable types are specified earlier in the list.

