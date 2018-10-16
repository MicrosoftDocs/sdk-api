---
UID: NS:fwpmtypes.FWPM_PROVIDER_CONTEXT_CHANGE0_
title: FWPM_PROVIDER_CONTEXT_CHANGE0_
author: windows-sdk-content
description: Change notification dispatched to subscribers.
old-location: fwp\fwpm_provider_context_change0_struct.htm
tech.root: fwp
ms.assetid: 78786d91-1e2f-4846-9636-8d5d6acf5a7d
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: FWPM_PROVIDER_CONTEXT_CHANGE0, FWPM_PROVIDER_CONTEXT_CHANGE0 structure [Filtering], FWPM_PROVIDER_CONTEXT_CHANGE0_, fwp.fwpm_provider_context_change0_struct, fwpmtypes/FWPM_PROVIDER_CONTEXT_CHANGE0
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
 - FWPM_PROVIDER_CONTEXT_CHANGE0
product: Windows
targetos: Windows
req.typenames: FWPM_PROVIDER_CONTEXT_CHANGE0
req.redist: 
---

# FWPM_PROVIDER_CONTEXT_CHANGE0_ structure


## -description


The <b>FWPM_PROVIDER_CONTEXT_CHANGE0</b> structure contains a change notification dispatched to subscribers.


## -struct-fields




### -field changeType

Type of change.

See <a href="https://msdn.microsoft.com/244dd91d-f5fa-4f78-8082-04fc209a9071">FWPM_CHANGE_TYPE</a> for more information.


### -field providerContextKey

GUID of the provider context that changed.


### -field providerContextId

LUID of the provider context that changed.


## -remarks



<b>FWPM_PROVIDER_CONTEXT_CHANGE0</b> is a specific implementation of FWPM_PROVIDER_CONTEXT_CHANGE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/244dd91d-f5fa-4f78-8082-04fc209a9071">FWPM_CHANGE_TYPE</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

