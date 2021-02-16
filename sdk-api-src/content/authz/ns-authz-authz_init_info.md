---
UID: NS:authz._AUTHZ_INIT_INFO
title: AUTHZ_INIT_INFO (authz.h)
description: Defines the initialization information for the resource manager.
helpviewer_keywords: ["*PAUTHZ_INIT_INFO","AUTHZ_INIT_INFO","AUTHZ_INIT_INFO structure [Security]","PAUTHZ_INIT_INFO","PAUTHZ_INIT_INFO structure pointer [Security]","authz/AUTHZ_INIT_INFO","authz/PAUTHZ_INIT_INFO","security.authz_init_info"]
old-location: security\authz_init_info.htm
tech.root: security
ms.assetid: 30489BE7-5B95-413E-8134-039AD3220A50
ms.date: 12/05/2018
ms.keywords: '*PAUTHZ_INIT_INFO, AUTHZ_INIT_INFO, AUTHZ_INIT_INFO structure [Security], PAUTHZ_INIT_INFO, PAUTHZ_INIT_INFO structure pointer [Security], authz/AUTHZ_INIT_INFO, authz/PAUTHZ_INIT_INFO, security.authz_init_info'
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: AUTHZ_INIT_INFO, *PAUTHZ_INIT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AUTHZ_INIT_INFO
 - authz/_AUTHZ_INIT_INFO
 - PAUTHZ_INIT_INFO
 - authz/PAUTHZ_INIT_INFO
 - AUTHZ_INIT_INFO
 - authz/AUTHZ_INIT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Authz.h
api_name:
 - AUTHZ_INIT_INFO
---

# AUTHZ_INIT_INFO structure


## -description

The <b>AUTHZ_INIT_INFO</b> structure defines the initialization information for the resource manager.

## -struct-fields

### -field version

The version of the authorization resource manager initialization information structure. This must be set to AUTHZ_INIT_INFO_VERSION_V1 (1).

### -field szResourceManagerName

Pointer to a Unicode string that identifies the resource manager. This parameter can be <b>NULL</b> if the resource manager does not need a name.

### -field pfnDynamicAccessCheck

Pointer to an <a href="/windows/desktop/SecAuthZ/authzaccesscheckcallback">AuthzAccessCheckCallback</a> callback function that the resource manager calls each time it encounters a callback access control entry (ACE) during access control list (ACL) evaluation in <a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> or <a href="/windows/desktop/api/authz/nf-authz-authzcachedaccesscheck">AuthzCachedAccessCheck</a>. This parameter can be <b>NULL</b> if no access check callback function is used.

### -field pfnComputeDynamicGroups

Pointer to the <a href="/windows/desktop/SecAuthZ/authzcomputegroupscallback">AuthzComputeGroupsCallback</a> callback function called by the resource manager during initialization of an AuthzClientContext handle. This parameter can be <b>NULL</b> if no callback function is used to compute dynamic groups.

### -field pfnFreeDynamicGroups

Pointer to the <a href="/windows/desktop/SecAuthZ/authzfreegroupscallback">AuthzFreeGroupsCallback</a> callback function called by the resource manager to free security identifier (SID) attribute arrays allocated by the compute dynamic groups callback. This parameter can be <b>NULL</b> if no callback function is used to compute dynamic groups.

### -field pfnGetCentralAccessPolicy

Pointer to the <a href="/windows/desktop/SecAuthZ/authzgetcentralaccesspolicycallback-">AuthzGetCentralAccessPolicyCallback</a> callback function to be called by the resource manager to resolve any Central Access Policy ID ACE (<a href="/windows/desktop/api/winnt/ns-winnt-system_scoped_policy_id_ace">SYSTEM_SCOPED_POLICY_ID_ACE</a>) encountered by <a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> or <a href="/windows/desktop/api/authz/nf-authz-authzcachedaccesscheck">AuthzCachedAccessCheck</a>. If this parameter is <b>NULL</b>, the <b>AuthzAccessCheck</b> function will fall back to LSA to resolve the Central Access Policy ID ACE.

### -field pfnFreeCentralAccessPolicy

Pointer to the <a href="/windows/desktop/SecAuthZ/authzfreecentralaccesspolicycallback">AuthzFreeCentralAccessPolicyCallback</a> callback function called by the resource manager to free the Central Access Policy allocated by the callback to get a central access policy. This parameter can be <b>NULL</b> if no callback function is specified for pfnGetCentralAccessPolicy