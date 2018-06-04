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

# eAVEncMPVIntraVLCTable enumeration


## -description



Specifies which variable-length coding (VLC) table to use for entropy coding. This enumeration is used with the <a href="https://msdn.microsoft.com/caa17027-8f11-47d3-83da-7ca83b27c978">AVEncMPVIntraVLCTable</a> property.




## -enum-fields




### -field eAVEncMPVIntraVLCTable_Auto

The encoder selects the VLC table.


### -field eAVEncMPVIntraVLCTable_MPEG1

The encoder uses the MPEG-1 VLC table.


### -field eAVEncMPVIntraVLCTable_Alternate

The encoder uses the alternate "intra" VLC table for MPEG-2.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

