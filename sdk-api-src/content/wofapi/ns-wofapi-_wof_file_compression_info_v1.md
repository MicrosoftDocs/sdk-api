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

# _WOF_FILE_COMPRESSION_INFO_V1 structure


## -description


 Defines metadata specific to files provided by WOF_PROVIDER_FILE.


## -struct-fields




### -field Algorithm

Specifies the compression algorithm that is used to compress this file. Currently defined algorithms are: 

<table>
<tr>
<td>FILE_PROVIDER_COMPRESSION_XPRESS4K</td>
<td>Indicates that the data for the file should be compressed in 4kb chunks with the XPress algorithm. This algorithm is designed to be computationally lightweight, and provides for rapid access to data.</td>
</tr>
<tr>
<td>FILE_PROVIDER_COMPRESSION_LZX</td>
<td>Indicates that the data for the file should be compressed in 32kb chunks with the LZX algorithm. This algorithm is designed to be highly compact, and provides for small footprint for infrequently accessed data.</td>
</tr>
<tr>
<td>FILE_PROVIDER_COMPRESSION_XPRESS8K</td>
<td>Indicates that the data for the file should be compressed in 8kb chunks with the XPress algorithm.</td>
</tr>
<tr>
<td>FILE_PROVIDER_COMPRESSION_XPRESS16K</td>
<td>Indicates that the data for the file should be compressed in 16kb chunks with the XPress algorithm.</td>
</tr>
</table>
 


### -field Flags

Specifies flags for the operation. Reserved for future use, should be 0. 

