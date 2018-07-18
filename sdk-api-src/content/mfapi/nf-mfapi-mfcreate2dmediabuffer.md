---
UID: NF:mfapi.MFCreate2DMediaBuffer
title: MFCreate2DMediaBuffer function
author: windows-sdk-content
description: Creates a system-memory buffer object to hold 2D image data.
old-location: mf\mfcreate2dmediabuffer.htm
old-project: medfound
ms.assetid: 7D999070-87BD-46AF-A4F0-C0A23DC1C876
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: MFCreate2DMediaBuffer, MFCreate2DMediaBuffer function [Media Foundation], mf.mfcreate2dmediabuffer, mfapi/MFCreate2DMediaBuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - MFCreate2DMediaBuffer
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreate2DMediaBuffer function


## -description


Creates a system-memory buffer object to hold 2D image data.


## -parameters




### -param dwWidth [in]

Width of the image, in pixels.




### -param dwHeight [in]

Height of the image, in pixels.


### -param dwFourCC [in]

A <b>FOURCC</b> code or <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> value that specifies the video format. If you have a video subtype GUID, you can use the first <b>DWORD</b> of the subtype.




### -param fBottomUp [in]

If <b>TRUE,</b> the buffer's <a href="https://msdn.microsoft.com/32601f2e-ab91-4a65-bcf4-8e063e90fbb0">IMF2DBuffer::ContiguousCopyTo</a> method copies the buffer into a bottom-up format. The bottom-up format is compatible with GDI for uncompressed RGB images. If this parameter is <b>FALSE</b>, the <b>ContiguousCopyTo</b> method copies the buffer into a top-down format, which is compatible with DirectX. 



For more information about top-down versus bottom-up images, see <a href="https://msdn.microsoft.com/13cd1106-48b3-4522-ac09-8efbaab5c31d">Image Stride</a>.




### -param ppBuffer [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> interface.


## -returns



This function can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
Unrecognized video format.

</td>
</tr>
</table>
 




## -remarks



The returned buffer object also exposes the <a href="https://msdn.microsoft.com/BFA73B1A-F8A7-4100-9DBD-234CCA06F9F5">IMF2DBuffer2</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

