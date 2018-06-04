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

# FWPS_INBOUND_FRAGMENT_METADATA0_ structure


## -description


The <b>FWPS_INBOUND_FRAGMENT_METADATA0</b> structure describes the fragment data for a received packet
  fragment.
<div class="alert"><b>Note</b>  <b>FWPS_INBOUND_FRAGMENT_METADATA0</b> is a specific version of <b>FWPS_INBOUND_FRAGMENT_METADATA</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields




### -field fragmentIdentification

A value that identifies the packet to which the packet fragment belongs.


### -field fragmentOffset

A value that specifies the offset, in bytes, of the packet fragment from the beginning of the
     packet.


### -field fragmentLength

A value that specifies the length, in bytes, of the packet fragment.


## -remarks



The FWPS_INBOUND_FRAGMENT_METADATA0 structure contains valid data only if the
    FWPS_METADATA_FIELD_FRAGMENT_DATA flag is set in the 
    <b>currentMetadataValues</b> member of the 
    <a href="https://msdn.microsoft.com/fba7eb60-0d19-4bfd-b484-2e615d3e9237">
    FWPS_INCOMING_METADATA_VALUES0</a> structure that the filter engine passes to a callout's 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function.




## -see-also




<a href="https://msdn.microsoft.com/fba7eb60-0d19-4bfd-b484-2e615d3e9237">
   FWPS_INCOMING_METADATA_VALUES0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a>
 

 

