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

# eAVDDSurroundMode enumeration


## -description



Specifies whether the audio is encoded in Dolby Surround. This enumeration is used with the <a href="https://msdn.microsoft.com/b33839c8-4829-4d90-94de-e461772d3e94">AVDDSurroundMode</a> property.




## -enum-fields




### -field eAVDDSurroundMode_NotIndicated

The bit stream does not indicate whether the audio is encoded in Dolby Surround.


### -field eAVDDSurroundMode_No

The bit stream is not encoded in Dolby Surround.


### -field eAVDDSurroundMode_Yes

The bit stream is encoded in Dolby Surround.


## -remarks



If the audio stream is Dolby AC-3, this property reflects the value of the dsurmod field in the bit stream.

<table>
<tr>
<th>
              Bit field
            </th>
<th>
              Value
            </th>
</tr>
<tr>
<td>00</td>
<td>eAVDDSurroundMode_NotIndicated</td>
</tr>
<tr>
<td>01</td>
<td>eAVDDSurroundMode_No</td>
</tr>
<tr>
<td>10</td>
<td>eAVDDSurroundMode_Yes</td>
</tr>
</table>
 

If the audio stream is any other format, the value is eAVDDSurroundMode_No.




## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

