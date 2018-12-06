---
UID: NF:strmif.IDDrawExclModeVideo.SetDDrawSurface
title: IDDrawExclModeVideo::SetDDrawSurface
author: windows-sdk-content
description: The SetDDrawSurface method specifies the DirectDraw surface to be used in subsequent drawing.
old-location: dshow\iddrawexclmodevideo_setddrawsurface.htm
tech.root: DirectShow
ms.assetid: a897c147-044d-44e2-9029-bd62c74483d2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDDrawExclModeVideo interface [DirectShow],SetDDrawSurface method, IDDrawExclModeVideo.SetDDrawSurface, IDDrawExclModeVideo::SetDDrawSurface, IDDrawExclModeVideoSetDDrawSurface, SetDDrawSurface, SetDDrawSurface method [DirectShow], SetDDrawSurface method [DirectShow],IDDrawExclModeVideo interface, dshow.iddrawexclmodevideo_setddrawsurface, strmif/IDDrawExclModeVideo::SetDDrawSurface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
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
 - IDDrawExclModeVideo.SetDDrawSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDDrawExclModeVideo::SetDDrawSurface


## -description



The <code>SetDDrawSurface</code> method specifies the DirectDraw surface to be used in subsequent drawing.




## -parameters




### -param pDDrawSurface [in]

Pointer to the <b>IDirectDrawSurface</b> interface on the surface to use.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

The current DirectShow implementation return values include the following.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_INVALIDARG</dt>
</dl>
</td>
<td width="60%">
Argument is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>A DirectDraw error code</dt>
</dl>
</td>
<td width="60%">
A DirectDraw error is encountered when trying to set the specified surface on the Overlay Mixer.

</td>
</tr>
</table>
 




## -remarks



A game application can use this to share its DirectDraw surface with the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter so that the video can be drawn in a specified surface. This surface must be associated with the object specified in <a href="https://msdn.microsoft.com/fce1b5df-c3df-475c-adde-392c25d05e4c">IDDrawExclModeVideo::SetDDrawObject</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a846a07-f513-49e7-85e8-192a5c211515">IDDrawExclModeVideo Interface</a>
 

 

