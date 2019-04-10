---
UID: NF:videoacc.IAMVideoAcceleratorNotify.GetUncompSurfacesInfo
title: IAMVideoAcceleratorNotify::GetUncompSurfacesInfo (videoacc.h)
author: windows-sdk-content
description: The GetUncompSurfacesInfo method queries the decoder for the number of uncompressed surfaces to allocate and the pixel format.
old-location: dshow\iamvideoacceleratornotify_getuncompsurfacesinfo.htm
tech.root: DirectShow
ms.assetid: ee8cbe71-6ac3-4f41-a9af-f372f825485d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetUncompSurfacesInfo, GetUncompSurfacesInfo method [DirectShow], GetUncompSurfacesInfo method [DirectShow],IAMVideoAcceleratorNotify interface, IAMVideoAcceleratorNotify interface [DirectShow],GetUncompSurfacesInfo method, IAMVideoAcceleratorNotify.GetUncompSurfacesInfo, IAMVideoAcceleratorNotify::GetUncompSurfacesInfo, IAMVideoAcceleratorNotifyGetUncompSurfacesInfo, dshow.iamvideoacceleratornotify_getuncompsurfacesinfo, videoacc/IAMVideoAcceleratorNotify::GetUncompSurfacesInfo
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
 - IAMVideoAcceleratorNotify.GetUncompSurfacesInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoAcceleratorNotify::GetUncompSurfacesInfo


## -description



The <b>GetUncompSurfacesInfo</b> method queries the decoder for the number of uncompressed surfaces to allocate and the pixel format.




## -parameters




### -param pGuid [in]

Pointer to a GUID that specifies the DXVA profile in use.


### -param pUncompBufferInfo [in, out]

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dd373448(v=VS.85).aspx">AMVAUncompBufferInfo</a> structure. The decoder fills in this structure with the decoder's requirements for the minimum and maximum number of surfaces and the pixel format.

To get the list of supported pixel formats, the decoder should call <a href="https://msdn.microsoft.com/en-us/library/Dd376007(v=VS.85).aspx">IAMVideoAccelerator::GetUncompFormatsSupported</a>.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface. <b>HRESULT</b> can include one of the following standard constants, or other values not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Argument is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
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
</table>
 




## -remarks



After the video renderer allocates the uncompressed surfaces, it calls the decoder's <a href="https://msdn.microsoft.com/en-us/library/Dd375996(v=VS.85).aspx">IAMVideoAcceleratorNotify::SetUncompSurfacesInfo</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd375993(v=VS.85).aspx">IAMVideoAcceleratorNotify Interface</a>
 

 

