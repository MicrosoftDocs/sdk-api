---
UID: NF:amvideo.IFullScreenVideoEx.GetCaption
title: IFullScreenVideoEx::GetCaption (amvideo.h)
author: windows-sdk-content
description: The GetCaption method retrieves the caption associated with the full-screen window.
old-location: dshow\ifullscreenvideoex_getcaption.htm
tech.root: DirectShow
ms.assetid: 0757da34-cfc5-4a40-9ad0-03bd016ad828
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCaption, GetCaption method [DirectShow], GetCaption method [DirectShow],IFullScreenVideoEx interface, IFullScreenVideoEx interface [DirectShow],GetCaption method, IFullScreenVideoEx.GetCaption, IFullScreenVideoEx::GetCaption, IFullScreenVideoGetCaption, amvideo/IFullScreenVideoEx::GetCaption, dshow.ifullscreenvideoex_getcaption
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
 - IFullScreenVideoEx.GetCaption
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFullScreenVideoEx::GetCaption


## -description



The <code>GetCaption</code> method retrieves the caption associated with the full-screen window.




## -parameters




### -param pstrCaption [out]

Pointer to a <b>BSTR</b> that receives the caption.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



The caption is visible when the window is minimized.

The caller must release the returned string, by calling the <b>SysFreeString</b> function.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390056(v=VS.85).aspx">IFullScreenVideoEx Interface</a>
 

 

