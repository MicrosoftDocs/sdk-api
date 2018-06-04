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

# tagMETAHEADER structure


## -description



The <b>METAHEADER</b> structure contains information about a Windows-format metafile.




## -struct-fields




### -field mtType

Specifies whether the metafile is in memory or recorded in a disk file. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>1</td>
<td>Metafile is in memory.</td>
</tr>
<tr>
<td>2</td>
<td>Metafile is in a disk file.</td>
</tr>
</table>
 


### -field mtHeaderSize

The size, in words, of the metafile header.


### -field mtVersion

The system version number. The version number for metafiles that support device-independent bitmaps (DIBs) is 0x0300. Otherwise, the version number is 0x0100.


### -field mtSize

The size, in words, of the file.


### -field mtNoObjects

The maximum number of objects that exist in the metafile at the same time.


### -field mtMaxRecord

The size, in words, of the largest record in the metafile.


### -field mtNoParameters

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/7c5d6e97-dff1-4c80-a7d3-082413dca469">METARECORD</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

