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

# FWPS_DISCARD_METADATA0_ structure


## -description


The <b>FWPS_DISCARD_METADATA0</b> structure describes the data that was discarded by the filter engine, a
  network layer, or a transport layer.
<div class="alert"><b>Note</b>  <b>FWPS_DISCARD_METADATA0</b> is a specific version of <b>FWPS_DISCARD_METADATA</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields




### -field discardModule

An 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff551236">FWPS_DISCARD_MODULE0</a> type that indicates
     the type of module that discarded the data.


### -field discardReason

A UINT32 value that specifies why the data was discarded. For a description of the discard reason
     identifiers for each type of module, see 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff546441">Discard Reason Identifiers</a>.


### -field filterId

A UINT64 value that specifies the run-time identifier for the filter in the filter engine that
     caused the data to be discarded.


## -remarks



The FWPS_DISCARD_METADATA0 structure contains valid data only if the
    FWPS_METADATA_FIELD_DISCARD_REASON flag is set in the 
    <b>currentMetadataValues</b> member of the 
    <a href="https://msdn.microsoft.com/fba7eb60-0d19-4bfd-b484-2e615d3e9237">
    FWPS_INCOMING_METADATA_VALUES0</a> structure that the filter engine passes to a callout's 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551236">FWPS_DISCARD_MODULE0</a>



<a href="https://msdn.microsoft.com/fba7eb60-0d19-4bfd-b484-2e615d3e9237">
   FWPS_INCOMING_METADATA_VALUES0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a>
 

 

