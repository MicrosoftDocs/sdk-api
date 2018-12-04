---
UID: NF:videoacc.IAMVideoAccelerator.GetUncompFormatsSupported
title: IAMVideoAccelerator::GetUncompFormatsSupported
author: windows-sdk-content
description: The GetUncompFormatsSupported method gets a list of uncompressed pixel formats that can be rendered using a specified DirectX Video Acceleration (DXVA) profile.
old-location: dshow\iamvideoaccelerator_getuncompformatssupported.htm
tech.root: DirectShow
ms.assetid: 33f9a4ee-4de9-4853-9581-808d7a07bfc4
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetUncompFormatsSupported, GetUncompFormatsSupported method [DirectShow], GetUncompFormatsSupported method [DirectShow],IAMVideoAccelerator interface, IAMVideoAccelerator interface [DirectShow],GetUncompFormatsSupported method, IAMVideoAccelerator.GetUncompFormatsSupported, IAMVideoAccelerator::GetUncompFormatsSupported, IAMVideoAcceleratorGetUncompFormatsSupported, dshow.iamvideoaccelerator_getuncompformatssupported, videoacc/IAMVideoAccelerator::GetUncompFormatsSupported
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: videoacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoAccelerator.GetUncompFormatsSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoAccelerator::GetUncompFormatsSupported


## -description



The <b>GetUncompFormatsSupported</b> method gets a list of uncompressed pixel formats that can be rendered using a specified DirectX Video Acceleration (DXVA) profile.




## -parameters




### -param pGuid [in]

Pointer to a GUID that specifies the DXVA profile. To get a list of supported profiles, call 
          <a href="https://msdn.microsoft.com/808ba120-f0e1-4348-94e7-69a27c77cf42">IAMVideoAccelerator::GetVideoAcceleratorGUIDs</a>.


### -param pdwNumFormatsSupported [in, out]

On input, specifies the number of elements in the <i>pFormatsSupported</i> array.
            If <i>pFormatsSupported</i> is <b>NULL</b>, the value of <code>*pdwNumFormatsSupported</code> must be zero.

On output, if <i>pFormatsSupported</i> is <b>NULL</b>, <i>pdwNumFormatsSupported</i> receives the number of supported pixel formats. Otherwise, <i>pdwNumFormatsSupported</i> receives the actual number of pixel formats copied to the <i>pFormatsSupported</i> array.


### -param pFormatsSupported [in, out]

Address of an array of <b>DDPIXELFORMAT</b> structures, or <b>NULL</b>. If the value is non-<b>NULL</b>, the array receives a list of pixel formats.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DDERR_MOREDATA</b></dt>
</dl>
</td>
<td width="60%">
The method returned fewer formats than the total number that are supported, because the array was too small. Although this value is a failure code, you can ignore the error if you intentionally allocated a smaller array.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



Call this method twice. On the first call, set <i>pFormatsSupported</i> to <b>NULL</b>. The <i>pdwNumFormatsSupported</i> parameter receives the number of formats. Allocate an array of <b>DDPIXELFORMAT</b> structures with the required size, and call the method again. This time, set <i>pFormatsSupported</i> to the address of the array. The method fills the array with the list of pixel formats.

The driver should return the formats in decreasing order of preference, with the most preferred format listed first.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>



<a href="https://msdn.microsoft.com/78e0a165-5a19-4dca-8d6c-445345772824">IAMVideoAccelerator Interface</a>
 

 

