---
UID: NS:ntsecapi._POLICY_LSA_SERVER_ROLE_INFO
title: POLICY_LSA_SERVER_ROLE_INFO (ntsecapi.h)
description: Used to set and query the role of an LSA server.
helpviewer_keywords: ["*PPOLICY_LSA_SERVER_ROLE_INFO","POLICY_LSA_SERVER_ROLE_INFO","POLICY_LSA_SERVER_ROLE_INFO structure [Security]","PPOLICY_LSA_SERVER_ROLE_INFO","PPOLICY_LSA_SERVER_ROLE_INFO structure pointer [Security]","_POLICY_LSA_SERVER_ROLE_INFO","_lsa_policy_lsa_server_role_info","ntsecapi/POLICY_LSA_SERVER_ROLE_INFO","ntsecapi/PPOLICY_LSA_SERVER_ROLE_INFO","security.policy_lsa_server_role_info"]
old-location: security\policy_lsa_server_role_info.htm
tech.root: security
ms.assetid: f66abe33-d8c8-45b8-9b94-d6890d786aaa
ms.date: 12/05/2018
ms.keywords: '*PPOLICY_LSA_SERVER_ROLE_INFO, POLICY_LSA_SERVER_ROLE_INFO, POLICY_LSA_SERVER_ROLE_INFO structure [Security], PPOLICY_LSA_SERVER_ROLE_INFO, PPOLICY_LSA_SERVER_ROLE_INFO structure pointer [Security], _POLICY_LSA_SERVER_ROLE_INFO, _lsa_policy_lsa_server_role_info, ntsecapi/POLICY_LSA_SERVER_ROLE_INFO, ntsecapi/PPOLICY_LSA_SERVER_ROLE_INFO, security.policy_lsa_server_role_info'
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
targetos: Windows
req.typenames: POLICY_LSA_SERVER_ROLE_INFO, *PPOLICY_LSA_SERVER_ROLE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _POLICY_LSA_SERVER_ROLE_INFO
 - ntsecapi/_POLICY_LSA_SERVER_ROLE_INFO
 - PPOLICY_LSA_SERVER_ROLE_INFO
 - ntsecapi/PPOLICY_LSA_SERVER_ROLE_INFO
 - POLICY_LSA_SERVER_ROLE_INFO
 - ntsecapi/POLICY_LSA_SERVER_ROLE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - POLICY_LSA_SERVER_ROLE_INFO
---

# POLICY_LSA_SERVER_ROLE_INFO structure


## -description

The <b>POLICY_LSA_SERVER_ROLE_INFO</b> structure is used to set and query the role of an LSA server. The <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy">LsaQueryInformationPolicy</a> and <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy">LsaSetInformationPolicy</a> functions use this structure when their <i>InformationClass</i> parameters are set to <b>PolicyLsaServerRoleInformation</b>.

## -struct-fields

### -field LsaServerRole

Specifies one of the values from the 
<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-policy_lsa_server_role">POLICY_LSA_SERVER_ROLE</a> enumeration type to indicate a primary or backup LSA server.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy">LsaQueryInformationPolicy</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy">LsaSetInformationPolicy</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-policy_information_class">POLICY_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-policy_lsa_server_role">POLICY_LSA_SERVER_ROLE</a>