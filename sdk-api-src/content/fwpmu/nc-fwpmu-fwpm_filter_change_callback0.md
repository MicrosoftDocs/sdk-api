---
UID: NC:fwpmu.FWPM_FILTER_CHANGE_CALLBACK0
title: FWPM_FILTER_CHANGE_CALLBACK0
author: windows-driver-content
description: Is used to added custom behavior to the filter change notification process.
old-location: fwp\fwpm_filter_change_callback0_func.htm
old-project: FWP
ms.assetid: 6c0c41d7-ff84-4ae3-b9e0-ebc52cc6273d
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: FWPM_FILTER_CHANGE_CALLBACK0, FWPM_FILTER_CHANGE_CALLBACK0 function pointer [Filtering], fwp.fwpm_filter_change_callback0_func, fwpmu/FWPM_FILTER_CHANGE_CALLBACK0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: fwpmu.h
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
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Fwpmu.h
api_name:
-	FWPM_FILTER_CHANGE_CALLBACK0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_FILTER_CHANGE_CALLBACK0 callback


## -description


The <b>FWPM_FILTER_CHANGE_CALLBACK0</b> function is used to added custom behavior to the filter change notification process.


## -parameters




### -param *context [in]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter passed to the <a href="https://msdn.microsoft.com/6dafce5d-239f-44b6-a24b-2b5646bfe4ec">FwpmFilterSubscribeChanges0</a> function.


### -param *change [in]

Type: <b>const <a href="https://msdn.microsoft.com/01c58002-5506-4e2a-ae85-30b16aad2dd6">FWPM_FILTER_CHANGE0</a>*</b>

The change notification information.


## -returns



This function pointer does not return a value.




## -remarks



Call <a href="https://msdn.microsoft.com/6dafce5d-239f-44b6-a24b-2b5646bfe4ec">FwpmFilterSubscribeChanges0</a> to register this callback function.

<b>FWPM_FILTER_CHANGE_CALLBACK0</b> is a specific implementation of FWPM_FILTER_CHANGE_CALLBACK. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/01c58002-5506-4e2a-ae85-30b16aad2dd6">FWPM_FILTER_CHANGE0</a>



<a href="https://msdn.microsoft.com/6dafce5d-239f-44b6-a24b-2b5646bfe4ec">FwpmFilterSubscribeChanges0</a>
 

 

