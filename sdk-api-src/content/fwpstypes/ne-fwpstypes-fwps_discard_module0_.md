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

# FWPS_DISCARD_MODULE0_ enumeration


## -description


The <b>FWPS_DISCARD_MODULE0</b> enumeration type specifies the type of module that discarded the
  data.
<div class="alert"><b>Note</b>  <b>FWPS_DISCARD_MODULE0</b> is a specific version of <b>FWPS_DISCARD_MODULE</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -enum-fields




### -field FWPS_DISCARD_MODULE_NETWORK

The data was discarded by the network layer.


### -field FWPS_DISCARD_MODULE_TRANSPORT

The data was discarded by the transport layer.


### -field FWPS_DISCARD_MODULE_GENERAL

The data was discarded by the filter engine.


### -field FWPS_DISCARD_MODULE_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
     header files and binaries.


## -remarks



The 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff551235">FWPS_DISCARD_METADATA0</a> structure
    contains a member of type FWPS_DISCARD_MODULE0 that specifies the type of module that discarded the
    data.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551235">FWPS_DISCARD_METADATA0</a>
 

 

