---
UID: NE:codecapi.eAVDDSurroundMode
title: eAVDDSurroundMode
author: windows-sdk-content
description: Specifies whether the audio is encoded in Dolby Surround. This enumeration is used with the AVDDSurroundMode property.
old-location: dshow\eavddsurroundmode.htm
tech.root: DirectShow
ms.assetid: daebcbdf-3a4d-494a-a403-8b075a6d393b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: codecapi/eAVDDSurroundMode, codecapi/eAVDDSurroundMode_No, codecapi/eAVDDSurroundMode_NotIndicated, codecapi/eAVDDSurroundMode_Yes, dshow.eavddsurroundmode, eAVDDSurroundMode, eAVDDSurroundMode enumeration [DirectShow], eAVDDSurroundModeEnumeration, eAVDDSurroundMode_No, eAVDDSurroundMode_NotIndicated, eAVDDSurroundMode_Yes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - codecapi.h
api_name:
 - eAVDDSurroundMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<th>Bit field
            </th>
<th>Value
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



<a href="https://msdn.microsoft.com/en-us/library/Dd311953(v=VS.85).aspx">ICodecAPI Interface</a>
 

 

