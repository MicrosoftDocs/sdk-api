---
UID: NE:fwpmtypes.FWPM_VSWITCH_EVENT_TYPE_
title: FWPM_VSWITCH_EVENT_TYPE_
author: windows-driver-content
description: Specifies the type of a vSwitch event.
old-location: fwp\fwpm_vswitch_event_type.htm
old-project: FWP
ms.assetid: 1c421152-1085-4cf4-ab8c-631a2b800ec8
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: FWPM_VSWITCH_EVENT_DISABLED_FOR_INSPECTION, FWPM_VSWITCH_EVENT_ENABLED_FOR_INSPECTION, FWPM_VSWITCH_EVENT_FILTER_ADD_TO_INCOMPLETE_LAYER, FWPM_VSWITCH_EVENT_FILTER_ENGINE_NOT_IN_REQUIRED_POSITION, FWPM_VSWITCH_EVENT_FILTER_ENGINE_REORDER, FWPM_VSWITCH_EVENT_MAX, FWPM_VSWITCH_EVENT_TYPE, FWPM_VSWITCH_EVENT_TYPE enumeration [Filtering], FWPM_VSWITCH_EVENT_TYPE_, fwp.fwpm_vswitch_event_type, fwpmtypes/FWPM_VSWITCH_EVENT_DISABLED_FOR_INSPECTION, fwpmtypes/FWPM_VSWITCH_EVENT_ENABLED_FOR_INSPECTION, fwpmtypes/FWPM_VSWITCH_EVENT_FILTER_ADD_TO_INCOMPLETE_LAYER, fwpmtypes/FWPM_VSWITCH_EVENT_FILTER_ENGINE_NOT_IN_REQUIRED_POSITION, fwpmtypes/FWPM_VSWITCH_EVENT_FILTER_ENGINE_REORDER, fwpmtypes/FWPM_VSWITCH_EVENT_MAX, fwpmtypes/FWPM_VSWITCH_EVENT_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FWPM_VSWITCH_EVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Fwpmtypes.h
api_name:
-	FWPM_VSWITCH_EVENT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_VSWITCH_EVENT_TYPE_ enumeration


## -description


The <b>FWPM_VSWITCH_EVENT_TYPE</b> enumeration specifies the type of a vSwitch event.


## -enum-fields




### -field FWPM_VSWITCH_EVENT_FILTER_ADD_TO_INCOMPLETE_LAYER

The filter engine is not enabled on all vSwitch instances. As a result, the filter(s) being added may not be fully enforced.


### -field FWPM_VSWITCH_EVENT_FILTER_ENGINE_NOT_IN_REQUIRED_POSITION

The filter engine to which the filter(s) are being added is not in its required position (typically the first filtering extension in the vSwitch instance). As a result, the filter(s) could be bypassed.


### -field FWPM_VSWITCH_EVENT_ENABLED_FOR_INSPECTION

The filter engine is being enabled for the vSwitch instance.


### -field FWPM_VSWITCH_EVENT_DISABLED_FOR_INSPECTION

The filter engine is being disabled for the vSwitch instance.


### -field FWPM_VSWITCH_EVENT_FILTER_ENGINE_REORDER

The filter engine is being reordered and may not be in the
   required position to enforce committed filters.


### -field FWPM_VSWITCH_EVENT_MAX

Maximum value for testing purposes.


## -see-also




<a href="https://msdn.microsoft.com/39029412-18ce-426a-a79d-cf25ff0dfe0d">Windows Filtering Platform API Enumerated Types</a>
 

 

