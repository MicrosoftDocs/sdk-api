---
UID: NE:ntsecapi._POLICY_LSA_SERVER_ROLE
title: POLICY_LSA_SERVER_ROLE (ntsecapi.h)
description: Defines values that indicate the role of an LSA server.
helpviewer_keywords: ["*PPOLICY_LSA_SERVER_ROLE","POLICY_LSA_SERVER_ROLE","POLICY_LSA_SERVER_ROLE enumeration [Security]","PPOLICY_LSA_SERVER_ROLE","PPOLICY_LSA_SERVER_ROLE enumeration pointer [Security]","PolicyServerRoleBackup","PolicyServerRolePrimary","_lsa_policy_lsa_server_role","ntsecapi/POLICY_LSA_SERVER_ROLE","ntsecapi/PPOLICY_LSA_SERVER_ROLE","ntsecapi/PolicyServerRoleBackup","ntsecapi/PolicyServerRolePrimary","security.policy_lsa_server_role"]
old-location: security\policy_lsa_server_role.htm
tech.root: security
ms.assetid: a2bcc380-8873-436b-a0d6-e4deb23669bb
ms.date: 12/05/2018
ms.keywords: '*PPOLICY_LSA_SERVER_ROLE, POLICY_LSA_SERVER_ROLE, POLICY_LSA_SERVER_ROLE enumeration [Security], PPOLICY_LSA_SERVER_ROLE, PPOLICY_LSA_SERVER_ROLE enumeration pointer [Security], PolicyServerRoleBackup, PolicyServerRolePrimary, _lsa_policy_lsa_server_role, ntsecapi/POLICY_LSA_SERVER_ROLE, ntsecapi/PPOLICY_LSA_SERVER_ROLE, ntsecapi/PolicyServerRoleBackup, ntsecapi/PolicyServerRolePrimary, security.policy_lsa_server_role'
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
req.typenames: POLICY_LSA_SERVER_ROLE, *PPOLICY_LSA_SERVER_ROLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _POLICY_LSA_SERVER_ROLE
 - ntsecapi/_POLICY_LSA_SERVER_ROLE
 - PPOLICY_LSA_SERVER_ROLE
 - ntsecapi/PPOLICY_LSA_SERVER_ROLE
 - POLICY_LSA_SERVER_ROLE
 - ntsecapi/POLICY_LSA_SERVER_ROLE
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
 - POLICY_LSA_SERVER_ROLE
---

# POLICY_LSA_SERVER_ROLE enumeration


## -description

The <b>POLICY_LSA_SERVER_ROLE</b> enumeration type defines values that indicate the role of an LSA server. The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy">LsaQueryInformationPolicy</a> and 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy">LsaSetInformationPolicy</a> functions use this enumeration type when their <i>InformationClass</i> parameters are set to <b>PolicyLsaServerRoleInformation</b>.

## -enum-fields

### -field PolicyServerRoleBackup:2

Indicates a backup LSA server.

### -field PolicyServerRolePrimary

Indicates a primary LSA server, a workstation, or a standalone computer.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy">LsaQueryInformationPolicy</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy">LsaSetInformationPolicy</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_lsa_server_role_info">POLICY_LSA_SERVER_ROLE_INFO</a>
