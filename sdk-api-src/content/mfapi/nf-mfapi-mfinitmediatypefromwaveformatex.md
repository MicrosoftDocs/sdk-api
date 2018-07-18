---
UID: NF:mfapi.MFInitMediaTypeFromWaveFormatEx
title: MFInitMediaTypeFromWaveFormatEx function
author: windows-sdk-content
description: Initializes a media type from a WAVEFORMATEX structure.
old-location: mf\mfinitmediatypefromwaveformatex.htm
old-project: medfound
ms.assetid: 91a201a6-06cf-4445-ad62-fdabb3848d51
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 91a201a6-06cf-4445-ad62-fdabb3848d51, MFInitMediaTypeFromWaveFormatEx, MFInitMediaTypeFromWaveFormatEx function [Media Foundation], mf.mfinitmediatypefromwaveformatex, mfapi/MFInitMediaTypeFromWaveFormatEx
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFInitMediaTypeFromWaveFormatEx
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFInitMediaTypeFromWaveFormatEx function


## -description



          Initializes a media type from a <b>WAVEFORMATEX</b> structure.
        


## -parameters




### -param pMFType

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type to initialize. To create the uninitialized media type object, call <a href="https://msdn.microsoft.com/05b0941e-03ce-4ced-9022-22b65d1c4b4c">MFCreateMediaType</a>.


### -param pWaveFormat

Pointer to a <b>WAVEFORMATEX</b> structure that describes the media type. The caller must fill in the structure members before calling this function.


### -param cbBufSize

Size of the <b>WAVEFORMATEX</b> structure, in bytes.


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
 




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/6aee18b8-79b1-47fb-816f-d1c2c77b3a03">Media Type Conversions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

