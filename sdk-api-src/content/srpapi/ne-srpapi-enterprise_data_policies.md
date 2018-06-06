---
UID: NE:srpapi.ENTERPRISE_DATA_POLICIES
title: ENTERPRISE_DATA_POLICIES
author: windows-sdk-content
description: Indicates whether the app is enlightened for Windows Information Protection (WIP) and whether the app is managed by policy.
old-location: edp\enterprise_data_policies.htm
old-project: EDP
ms.assetid: BCD039C9-88F6-495C-9AE4-B80D06B2557B
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EDP.enterprise_data_policies, ENTERPRISE_DATA_POLICIES, ENTERPRISE_DATA_POLICIES enumeration, ENTERPRISE_POLICY_ALLOWED, ENTERPRISE_POLICY_ENLIGHTENED, ENTERPRISE_POLICY_EXEMPT, ENTERPRISE_POLICY_NONE, srpapi/ENTERPRISE_DATA_POLICIES, srpapi/ENTERPRISE_POLICY_ALLOWED, srpapi/ENTERPRISE_POLICY_ENLIGHTENED, srpapi/ENTERPRISE_POLICY_EXEMPT, srpapi/ENTERPRISE_POLICY_NONE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: ENTERPRISE_DATA_POLICIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - srpapi.h
api_name:
 - ENTERPRISE_DATA_POLICIES
product: Windows
targetos: Windows
req.lib: Nmapi.lib
req.dll: Nmapi.dll
req.irql: 
req.product: Outlook Express 6.0
---

# ENTERPRISE_DATA_POLICIES enumeration


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]


<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Indicates whether the app is enlightened for Windows Information Protection (WIP) and whether the app is managed by policy. 


## -enum-fields




### -field ENTERPRISE_POLICY_NONE

The app is not managed by enterprise policy.


### -field ENTERPRISE_POLICY_ALLOWED

The app is allowed to access enterprise resources according to the enterprise policy.


### -field ENTERPRISE_POLICY_ENLIGHTENED

The app is enlightened (self-declared in the app's resource file).


### -field ENTERPRISE_POLICY_EXEMPT

The app is marked as exempt by the enterprise policy.

