---
UID: NF:strmif.IDDrawExclModeVideo.SetDDrawSurface
title: IDDrawExclModeVideo::SetDDrawSurface (strmif.h)
author: windows-sdk-content
description: The SetDDrawSurface method specifies the DirectDraw surface to be used in subsequent drawing.
old-location: dshow\iddrawexclmodevideo_setddrawsurface.htm
tech.root: DirectShow
ms.assetid: a897c147-044d-44e2-9029-bd62c74483d2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDDrawExclModeVideo interface [DirectShow],SetDDrawSurface method, IDDrawExclModeVideo.SetDDrawSurface, IDDrawExclModeVideo::SetDDrawSurface, IDDrawExclModeVideoSetDDrawSurface, SetDDrawSurface, SetDDrawSurface method [DirectShow], SetDDrawSurface method [DirectShow],IDDrawExclModeVideo interface, dshow.iddrawexclmodevideo_setddrawsurface, strmif/IDDrawExclModeVideo::SetDDrawSurface
ms.topic: method
f1_keywords: 
 - "strmif/IDDrawExclModeVideo.SetDDrawSurface"
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
ms.custom: 19H1
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



A game application can use this to share its DirectDraw surface with the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter so that the video can be drawn in a specified surface. This surface must be associated with the object specified in <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iddrawexclmodevideo-setddrawobject">IDDrawExclModeVideo::SetDDrawObject</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideo">IDDrawExclModeVideo Interface</a>
 

 

