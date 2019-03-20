---
UID: NS:fwpmtypes.FWPM_SUBLAYER_CHANGE0_
title: FWPM_SUBLAYER_CHANGE0 (fwpmtypes.h)
author: windows-sdk-content
description: Change notification dispatched to subscribers.
old-location: fwp\fwpm_sublayer_change0_struct.htm
tech.root: fwp
ms.assetid: f01593aa-e7b1-42f1-b523-2f9e6d6b631b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FWPM_SUBLAYER_CHANGE0, FWPM_SUBLAYER_CHANGE0 structure [Filtering], fwp.fwpm_sublayer_change0_struct, fwpmtypes/FWPM_SUBLAYER_CHANGE0
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
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_SUBLAYER_CHANGE0
product: Windows
targetos: Windows
req.typenames: FWPM_SUBLAYER_CHANGE0
req.redist: 
---

# FWPM_SUBLAYER_CHANGE0 structure


## -description


The <b>FWPM_SUBLAYER_CHANGE0</b> structure specifies a change notification dispatched to subscribers.


## -struct-fields




### -field changeType

Type of change as specified by <a href="https://msdn.microsoft.com/244dd91d-f5fa-4f78-8082-04fc209a9071">FWPM_CHANGE_TYPE</a>.


### -field subLayerKey

GUID of the sublayer that changed.


## -remarks



<b>FWPM_SUBLAYER_CHANGE0</b> is a specific implementation of FWPM_SUBLAYER_CHANGE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/244dd91d-f5fa-4f78-8082-04fc209a9071">FWPM_CHANGE_TYPE</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

