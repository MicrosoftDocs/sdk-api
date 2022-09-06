---
UID: NE:srpapi.__unnamed_enum_0
title: ENTERPRISE_DATA_POLICIES (srpapi.h)
description: Indicates whether the app is enlightened for Windows Information Protection (WIP) and whether the app is managed by policy.
helpviewer_keywords: ["EDP.enterprise_data_policies","ENTERPRISE_DATA_POLICIES","ENTERPRISE_DATA_POLICIES enumeration","ENTERPRISE_POLICY_ALLOWED","ENTERPRISE_POLICY_ENLIGHTENED","ENTERPRISE_POLICY_EXEMPT","ENTERPRISE_POLICY_NONE","srpapi/ENTERPRISE_DATA_POLICIES","srpapi/ENTERPRISE_POLICY_ALLOWED","srpapi/ENTERPRISE_POLICY_ENLIGHTENED","srpapi/ENTERPRISE_POLICY_EXEMPT","srpapi/ENTERPRISE_POLICY_NONE"]
old-location: edp\enterprise_data_policies.htm
tech.root: EDP
ms.assetid: BCD039C9-88F6-495C-9AE4-B80D06B2557B
ms.date: 12/05/2018
ms.keywords: EDP.enterprise_data_policies, ENTERPRISE_DATA_POLICIES, ENTERPRISE_DATA_POLICIES enumeration, ENTERPRISE_POLICY_ALLOWED, ENTERPRISE_POLICY_ENLIGHTENED, ENTERPRISE_POLICY_EXEMPT, ENTERPRISE_POLICY_NONE, srpapi/ENTERPRISE_DATA_POLICIES, srpapi/ENTERPRISE_POLICY_ALLOWED, srpapi/ENTERPRISE_POLICY_ENLIGHTENED, srpapi/ENTERPRISE_POLICY_EXEMPT, srpapi/ENTERPRISE_POLICY_NONE
req.header: srpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: ENTERPRISE_DATA_POLICIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ENTERPRISE_DATA_POLICIES
 - srpapi/ENTERPRISE_DATA_POLICIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - srpapi.h
api_name:
 - ENTERPRISE_DATA_POLICIES
---

# ENTERPRISE_DATA_POLICIES enumeration


## -description




<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Indicates whether the app is enlightened for Windows Information Protection (WIP) and whether the app is managed by policy.

## -enum-fields

### -field ENTERPRISE_POLICY_NONE:0x0

The app is not managed by enterprise policy.

### -field ENTERPRISE_POLICY_ALLOWED:0x1

The app is allowed to access enterprise resources according to the enterprise policy.

### -field ENTERPRISE_POLICY_ENLIGHTENED:0x2

The app is enlightened (self-declared in the app's resource file).

### -field ENTERPRISE_POLICY_EXEMPT:0x4

The app is marked as exempt by the enterprise policy.

