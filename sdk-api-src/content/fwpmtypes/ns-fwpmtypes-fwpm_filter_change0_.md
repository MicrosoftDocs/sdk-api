---
UID: NS:fwpmtypes.FWPM_FILTER_CHANGE0_
title: FWPM_FILTER_CHANGE0_
author: windows-sdk-content
description: Stores change notification dispatched to subscribers.
old-location: fwp\fwpm_filter_change0_struct.htm
old-project: FWP
ms.assetid: 01c58002-5506-4e2a-ae85-30b16aad2dd6
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: FWPM_FILTER_CHANGE0, FWPM_FILTER_CHANGE0 structure [Filtering], FWPM_FILTER_CHANGE0_, fwp.fwpm_filter_change0_struct, fwpmtypes/FWPM_FILTER_CHANGE0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FWPM_FILTER_CHANGE0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_FILTER_CHANGE0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_FILTER_CHANGE0_ structure


## -description



		The <b>FWPM_FILTER_CHANGE0</b> structure stores change notification dispatched to subscribers.


## -struct-fields




### -field changeType

A <a href="https://msdn.microsoft.com/244dd91d-f5fa-4f78-8082-04fc209a9071">FWPM_CHANGE_TYPE</a> value that specifies the type of change notification to be dispatched.


### -field filterKey

GUID of the filter that changed.


### -field filterId

LUID of the filter that changed.


## -remarks



<b>FWPM_FILTER_CHANGE0</b> is a specific implementation of FWPM_FILTER_CHANGE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/244dd91d-f5fa-4f78-8082-04fc209a9071">FWPM_CHANGE_TYPE</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

