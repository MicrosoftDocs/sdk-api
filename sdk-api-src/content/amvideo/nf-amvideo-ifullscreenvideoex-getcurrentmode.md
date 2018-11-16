---
UID: NF:amvideo.IFullScreenVideoEx.GetCurrentMode
title: IFullScreenVideoEx::GetCurrentMode
author: windows-sdk-content
description: The GetCurrentMode method retrieves the current display mode.
old-location: dshow\ifullscreenvideoex_getcurrentmode.htm
tech.root: DirectShow
ms.assetid: 036914da-4223-4601-9e4a-4c7840b7dd22
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetCurrentMode, GetCurrentMode method [DirectShow], GetCurrentMode method [DirectShow],IFullScreenVideoEx interface, IFullScreenVideoEx interface [DirectShow],GetCurrentMode method, IFullScreenVideoEx.GetCurrentMode, IFullScreenVideoEx::GetCurrentMode, IFullScreenVideoGetCurrentMode, amvideo/IFullScreenVideoEx::GetCurrentMode, dshow.ifullscreenvideoex_getcurrentmode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: amvideo.h
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
 - IFullScreenVideoEx.GetCurrentMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- amvideo.h
: 
- IFullScreenVideoEx.GetCurrentMode
: 
---

# IFullScreenVideoEx::GetCurrentMode


## -description



The <code>GetCurrentMode</code> method retrieves the current display mode.




## -parameters




### -param pMode [out]

Pointer to a variable that receives the index of the current video mode. Pass this index to the <a href="https://msdn.microsoft.com/c1a4aea8-8c48-4073-80ed-060db5adb514">IFullScreenVideoEx::GetModeInfo</a> method to obtain information about this mode, including the width, height, and bit depth.


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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The filter did not load DirectDraw.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4c9de58f-6ceb-4cf5-b1a5-d3e345e08190">IFullScreenVideoEx Interface</a>
 

 

