---
UID: NF:mfapi.MFCreateWaveFormatExFromMFMediaType
title: MFCreateWaveFormatExFromMFMediaType function
author: windows-sdk-content
description: Converts a Media Foundation audio media type to a WAVEFORMATEX structure.
old-location: mf\mfcreatewaveformatexfrommfmediatype.htm
tech.root: medfound
ms.assetid: b124bac2-90de-4358-a079-f509a89c3776
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: MFCreateWaveFormatExFromMFMediaType, MFCreateWaveFormatExFromMFMediaType function [Media Foundation], b124bac2-90de-4358-a079-f509a89c3776, mf.mfcreatewaveformatexfrommfmediatype, mfapi/MFCreateWaveFormatExFromMFMediaType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateWaveFormatExFromMFMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateWaveFormatExFromMFMediaType function


## -description



Converts a Media Foundation audio media type to a <b>WAVEFORMATEX</b> structure.




## -parameters




### -param pMFType

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type.


### -param ppWF

Receives a pointer to the <b>WAVEFORMATEX</b> structure. The caller must release the memory allocated for the structure by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


### -param pcbSize

Receives the size of the <b>WAVEFORMATEX</b> structure.


### -param Flags

Contains a flag from the <a href="https://msdn.microsoft.com/cd4a54f3-58e5-4e39-8615-e5037972c9c4">MFWaveFormatExConvertFlags</a> enumeration.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



If the <b>wFormatTag</b> member of the returned structure is <b>WAVE_FORMAT_EXTENSIBLE</b>, you can cast the pointer to a <b>WAVEFORMATEXTENSIBLE</b> structure.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/6aee18b8-79b1-47fb-816f-d1c2c77b3a03">Media Type Conversions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

