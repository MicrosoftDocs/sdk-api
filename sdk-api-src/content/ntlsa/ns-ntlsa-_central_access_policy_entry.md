---
UID: NS:ntlsa._CENTRAL_ACCESS_POLICY_ENTRY
title: "_CENTRAL_ACCESS_POLICY_ENTRY"
author: windows-driver-content
description: Represents a central access policy entry containing a list of security descriptors and staged security descriptors.
old-location: security\central_access_policy_entry.htm
old-project: SecAuthN
ms.assetid: 8667848D-096C-422E-B4A6-38CC406F0F4A
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: "*PCENTRAL_ACCESS_POLICY_ENTRY, CENTRAL_ACCESS_POLICY_ENTRY, CENTRAL_ACCESS_POLICY_ENTRY structure [Security], PCENTRAL_ACCESS_POLICY_ENTRY, PCENTRAL_ACCESS_POLICY_ENTRY structure pointer [Security], _CENTRAL_ACCESS_POLICY_ENTRY, ntlsa/CENTRAL_ACCESS_POLICY_ENTRY, ntlsa/PCENTRAL_ACCESS_POLICY_ENTRY, security.central_access_policy_entry"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: CENTRAL_ACCESS_POLICY_ENTRY, *PCENTRAL_ACCESS_POLICY_ENTRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntlsa.h
api_name:
-	CENTRAL_ACCESS_POLICY_ENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _CENTRAL_ACCESS_POLICY_ENTRY structure


## -description


Represents a central access policy entry containing a list of security descriptors and staged security descriptors.


## -struct-fields




### -field Name

The name of the central access policy entry.


### -field Description

The description of the central access policy entry.


### -field ChangeId

An identifier that can be used to version the central access policy entry.


### -field LengthAppliesTo

The length of the buffer pointed to by the <i>AppliesTo</i> field.


### -field AppliesTo

A resource condition in binary form.


### -field LengthSD

The length of the buffer pointed to by the <i>SD</i> field.


### -field SD

A buffer of security descriptors associated with the entry.


### -field LengthStagedSD

The length of the buffer pointed to by the <i>StagedSD</i> field.


### -field StagedSD

A buffer of staged security descriptors associated with the entry.


### -field Flags

This field is reserved.

