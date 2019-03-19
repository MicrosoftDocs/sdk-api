---
UID: NS:ntsecapi._POLICY_LSA_SERVER_ROLE_INFO
title: POLICY_LSA_SERVER_ROLE_INFO (ntsecapi.h)
author: windows-sdk-content
description: Used to set and query the role of an LSA server.
old-location: security\policy_lsa_server_role_info.htm
tech.root: SecMgmt
ms.assetid: f66abe33-d8c8-45b8-9b94-d6890d786aaa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PPOLICY_LSA_SERVER_ROLE_INFO, POLICY_LSA_SERVER_ROLE_INFO, POLICY_LSA_SERVER_ROLE_INFO structure [Security], PPOLICY_LSA_SERVER_ROLE_INFO, PPOLICY_LSA_SERVER_ROLE_INFO structure pointer [Security], _POLICY_LSA_SERVER_ROLE_INFO, _lsa_policy_lsa_server_role_info, ntsecapi/POLICY_LSA_SERVER_ROLE_INFO, ntsecapi/PPOLICY_LSA_SERVER_ROLE_INFO, security.policy_lsa_server_role_info"
ms.topic: struct
req.header: ntsecapi.h
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
 - Ntsecapi.h
api_name:
 - POLICY_LSA_SERVER_ROLE_INFO
product: Windows
targetos: Windows
req.typenames: POLICY_LSA_SERVER_ROLE_INFO, *PPOLICY_LSA_SERVER_ROLE_INFO
req.redist: 
---

# POLICY_LSA_SERVER_ROLE_INFO structure


## -description


The <b>POLICY_LSA_SERVER_ROLE_INFO</b> structure is used to set and query the role of an LSA server. The <a href="https://msdn.microsoft.com/2d543500-f639-4ef7-91f4-cdc5060dd567">LsaQueryInformationPolicy</a> and <a href="https://msdn.microsoft.com/2aa3b09e-2cd9-4a09-bfd6-b37c97266dcb">LsaSetInformationPolicy</a> functions use this structure when their <i>InformationClass</i> parameters are set to <b>PolicyLsaServerRoleInformation</b>.


## -struct-fields




### -field LsaServerRole

Specifies one of the values from the 
<a href="https://msdn.microsoft.com/a2bcc380-8873-436b-a0d6-e4deb23669bb">POLICY_LSA_SERVER_ROLE</a> enumeration type to indicate a primary or backup LSA server.


## -see-also




<a href="https://msdn.microsoft.com/2d543500-f639-4ef7-91f4-cdc5060dd567">LsaQueryInformationPolicy</a>



<a href="https://msdn.microsoft.com/2aa3b09e-2cd9-4a09-bfd6-b37c97266dcb">LsaSetInformationPolicy</a>



<a href="https://msdn.microsoft.com/b734b5e8-1ee9-436b-b2a9-210ae79fbaf5">POLICY_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/a2bcc380-8873-436b-a0d6-e4deb23669bb">POLICY_LSA_SERVER_ROLE</a>
 

 

