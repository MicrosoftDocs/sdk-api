---
UID: NF:control.IBasicVideo.GetVideoPaletteEntries
title: IBasicVideo::GetVideoPaletteEntries
author: windows-sdk-content
description: The GetVideoPaletteEntries method retrieves the palette colors for the video.
old-location: dshow\ibasicvideo_getvideopaletteentries.htm
tech.root: DirectShow
ms.assetid: 9a022bc5-56f5-41c0-940f-f9074791a353
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetVideoPaletteEntries, GetVideoPaletteEntries method [DirectShow], GetVideoPaletteEntries method [DirectShow],IBasicVideo interface, IBasicVideo interface [DirectShow],GetVideoPaletteEntries method, IBasicVideo.GetVideoPaletteEntries, IBasicVideo::GetVideoPaletteEntries, IBasicVideoGetVideoPaletteEntries, control/IBasicVideo::GetVideoPaletteEntries, dshow.ibasicvideo_getvideopaletteentries
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
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
 - IBasicVideo.GetVideoPaletteEntries
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBasicVideo::GetVideoPaletteEntries


## -description



The <code>GetVideoPaletteEntries</code> method retrieves the palette colors for the video.




## -parameters




### -param StartIndex [in]

Start index for the palette.


### -param Entries [in]

Number of palette entries to retrieve.


### -param pRetrieved [out]

Pointer to a variable that receives the number of entries returned in <i>pPallette</i>.


### -param pPalette [out]

Pointer to an array of <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structures of size <i>Entries</i>. Cast the pointer to a long pointer type. The method fills the array.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>VFW_E_NO_PALETTE_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
No palette is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The Video Renderer's input pin is not connected.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/14f45bdc-2271-459d-b165-c860c8fc3e0b">IBasicVideo Interface</a>
 

 

