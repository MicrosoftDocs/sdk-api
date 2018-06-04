---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

