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

# FWPS_INCOMING_VALUES0_ structure


## -description


The <b>FWPS_INCOMING_VALUES0</b> structure defines data values that are passed by the filter engine to a
  callout's 
  <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function.
<div class="alert"><b>Note</b>  <b>FWPS_INCOMING_VALUES0</b> is a specific version of <b>FWPS_INCOMING_VALUES</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields




### -field layerId

The run-time filtering layer identifier for the filtering layer at which the data values were
     obtained. For more information, see 
     <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa366492">Run-time Filtering Layer
     Identifiers</a>.


### -field valueCount

The number of 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552398">FWPS_INCOMING_VALUE0</a> structures in the
     array pointed to by the 
     <b>incomingValue</b> member.


### -field incomingValue

A pointer to an array of 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552398">FWPS_INCOMING_VALUE0</a> structures that
     contain the data values.


## -remarks



The filter engine passes a pointer to an FWPS_INCOMING_VALUES0 structure to a callout's 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552398">FWPS_INCOMING_VALUE0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a>
 

 

