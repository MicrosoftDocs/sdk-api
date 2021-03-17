---
UID: NS:ntlsa._CENTRAL_ACCESS_POLICY
title: CENTRAL_ACCESS_POLICY (ntlsa.h)
description: Represents a central access policy that contains a set of central access policy entries.
helpviewer_keywords: ["*PCENTRAL_ACCESS_POLICY","CENTRAL_ACCESS_POLICY","CENTRAL_ACCESS_POLICY structure [Security]","PCENTRAL_ACCESS_POLICY","PCENTRAL_ACCESS_POLICY structure pointer [Security]","_CENTRAL_ACCESS_POLICY","ntlsa/CENTRAL_ACCESS_POLICY","ntlsa/PCENTRAL_ACCESS_POLICY","security.central_access_policy"]
old-location: security\central_access_policy.htm
tech.root: security
ms.assetid: C1C2E8AE-0B7F-4620-9C27-31DAF683E342
ms.date: 12/05/2018
ms.keywords: '*PCENTRAL_ACCESS_POLICY, CENTRAL_ACCESS_POLICY, CENTRAL_ACCESS_POLICY structure [Security], PCENTRAL_ACCESS_POLICY, PCENTRAL_ACCESS_POLICY structure pointer [Security], _CENTRAL_ACCESS_POLICY, ntlsa/CENTRAL_ACCESS_POLICY, ntlsa/PCENTRAL_ACCESS_POLICY, security.central_access_policy'
req.header: ntlsa.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CENTRAL_ACCESS_POLICY, *PCENTRAL_ACCESS_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CENTRAL_ACCESS_POLICY
 - ntlsa/_CENTRAL_ACCESS_POLICY
 - PCENTRAL_ACCESS_POLICY
 - ntlsa/PCENTRAL_ACCESS_POLICY
 - CENTRAL_ACCESS_POLICY
 - ntlsa/CENTRAL_ACCESS_POLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntlsa.h
api_name:
 - CENTRAL_ACCESS_POLICY
---

# CENTRAL_ACCESS_POLICY structure


## -description

Represents a central access policy that contains a set of central access policy entries.

## -struct-fields

### -field CAPID

The identifier of the central access policy.

### -field Name

The name of the central access policy.

### -field Description

The description of the central access policy.

### -field ChangeId

An identifier that can be used to version the central access policy.

### -field Flags

Reserved.

### -field CAPECount

The length of the buffer pointed to by the <i>CAPEs</i> field.

### -field CAPEs

Pointer to a buffer of <a href="/windows/desktop/api/ntlsa/ns-ntlsa-central_access_policy_entry">CENTRAL_ACCESS_POLICY_ENTRY</a> pointers.