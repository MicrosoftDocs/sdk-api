---
UID: NS:ntsecapi._POLICY_AUDIT_SID_ARRAY
title: POLICY_AUDIT_SID_ARRAY (ntsecapi.h)
description: Specifies an array of SID structures that represent Windows users or groups.
helpviewer_keywords: ["*PPOLICY_AUDIT_SID_ARRAY","POLICY_AUDIT_SID_ARRAY","POLICY_AUDIT_SID_ARRAY structure [Security]","PPOLICY_AUDIT_SID_ARRAY","PPOLICY_AUDIT_SID_ARRAY structure pointer [Security]","ntsecapi/POLICY_AUDIT_SID_ARRAY","ntsecapi/PPOLICY_AUDIT_SID_ARRAY","security.policy_audit_sid_array"]
old-location: security\policy_audit_sid_array.htm
tech.root: security
ms.assetid: 22f4255c-331a-4327-84d8-e905c7e419b6
ms.date: 12/05/2018
ms.keywords: '*PPOLICY_AUDIT_SID_ARRAY, POLICY_AUDIT_SID_ARRAY, POLICY_AUDIT_SID_ARRAY structure [Security], PPOLICY_AUDIT_SID_ARRAY, PPOLICY_AUDIT_SID_ARRAY structure pointer [Security], ntsecapi/POLICY_AUDIT_SID_ARRAY, ntsecapi/PPOLICY_AUDIT_SID_ARRAY, security.policy_audit_sid_array'
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: POLICY_AUDIT_SID_ARRAY, *PPOLICY_AUDIT_SID_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _POLICY_AUDIT_SID_ARRAY
 - ntsecapi/_POLICY_AUDIT_SID_ARRAY
 - PPOLICY_AUDIT_SID_ARRAY
 - ntsecapi/PPOLICY_AUDIT_SID_ARRAY
 - POLICY_AUDIT_SID_ARRAY
 - ntsecapi/POLICY_AUDIT_SID_ARRAY
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
 - POLICY_AUDIT_SID_ARRAY
---

# POLICY_AUDIT_SID_ARRAY structure


## -description

The <b>POLICY_AUDIT_SID_ARRAY</b> structure specifies an array of <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structures that represent Windows users or groups.

## -struct-fields

### -field UsersCount

The number of <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structures in the <b>UserSidArray</b> array.

### -field UserSidArray.size_is

### -field UserSidArray.size_is.UsersCount

### -field UserSidArray

A pointer to an array of pointers to <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structures that specify Windows users or groups.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditenumerateperuserpolicy">AuditEnumeratePerUserPolicy</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>