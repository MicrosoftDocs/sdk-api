---
UID: NF:strmif.IDDrawExclModeVideo.GetDDrawSurface
title: IDDrawExclModeVideo::GetDDrawSurface (strmif.h)
description: The GetDDrawSurface method retrieves the DirectDraw surface being used by the Overlay Mixer.
helpviewer_keywords: ["GetDDrawSurface","GetDDrawSurface method [DirectShow]","GetDDrawSurface method [DirectShow]","IDDrawExclModeVideo interface","IDDrawExclModeVideo interface [DirectShow]","GetDDrawSurface method","IDDrawExclModeVideo.GetDDrawSurface","IDDrawExclModeVideo::GetDDrawSurface","IDDrawExclModeVideoGetDDrawSurface","dshow.iddrawexclmodevideo_getddrawsurface","strmif/IDDrawExclModeVideo::GetDDrawSurface"]
old-location: dshow\iddrawexclmodevideo_getddrawsurface.htm
tech.root: dshow
ms.assetid: 0fb29af3-5f6f-4502-8785-72c64f72fec4
ms.date: 12/05/2018
ms.keywords: GetDDrawSurface, GetDDrawSurface method [DirectShow], GetDDrawSurface method [DirectShow],IDDrawExclModeVideo interface, IDDrawExclModeVideo interface [DirectShow],GetDDrawSurface method, IDDrawExclModeVideo.GetDDrawSurface, IDDrawExclModeVideo::GetDDrawSurface, IDDrawExclModeVideoGetDDrawSurface, dshow.iddrawexclmodevideo_getddrawsurface, strmif/IDDrawExclModeVideo::GetDDrawSurface
f1_keywords:
- strmif/IDDrawExclModeVideo.GetDDrawSurface
dev_langs:
- c++
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
- IDDrawExclModeVideo.GetDDrawSurface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDDrawExclModeVideo::GetDDrawSurface


## -description



The <code>GetDDrawSurface</code> method retrieves the DirectDraw surface being used by the Overlay Mixer.




## -parameters




### -param ppDDrawSurface [out]

Address of a pointer to the <b>IDirectDrawSurface</b> interface that is being used by the Overlay Mixer.


### -param pbUsingExternal [out]

Pointer to a variable that receives a Boolean value. It receives the value <b>TRUE</b> if the Overlay Mixer is using a DirectDraw surface specified by <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface">IDDrawExclModeVideo::SetDDrawSurface</a>, or <b>FALSE</b> otherwise.


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
<dt><b>A DirectDraw error code</b></dt>
</dl>
</td>
<td width="60%">
A DirectDraw error is encountered when trying to set the specified surface on the Overlay Mixer.

</td>
</tr>
</table>
 




## -remarks



If the filter graph has not set a DirectDraw surface and the Overlay Mixer has not yet allocated one, then <i>pDDrawSurface</i> will be set to <b>NULL</b> and <i>pdUsingExternal</i> will be set to <b>FALSE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideo">IDDrawExclModeVideo Interface</a>
 

 

