---
UID: NF:strmif.IDDrawExclModeVideo.SetDDrawObject
title: IDDrawExclModeVideo::SetDDrawObject (strmif.h)
description: The SetDDrawObject method sets the DirectDraw object to be used in subsequent drawing.
helpviewer_keywords: ["IDDrawExclModeVideo interface [DirectShow]","SetDDrawObject method","IDDrawExclModeVideo.SetDDrawObject","IDDrawExclModeVideo::SetDDrawObject","IDDrawExclModeVideoSetDDrawObject","SetDDrawObject","SetDDrawObject method [DirectShow]","SetDDrawObject method [DirectShow]","IDDrawExclModeVideo interface","dshow.iddrawexclmodevideo_setddrawobject","strmif/IDDrawExclModeVideo::SetDDrawObject"]
old-location: dshow\iddrawexclmodevideo_setddrawobject.htm
tech.root: dshow
ms.assetid: fce1b5df-c3df-475c-adde-392c25d05e4c
ms.date: 12/05/2018
ms.keywords: IDDrawExclModeVideo interface [DirectShow],SetDDrawObject method, IDDrawExclModeVideo.SetDDrawObject, IDDrawExclModeVideo::SetDDrawObject, IDDrawExclModeVideoSetDDrawObject, SetDDrawObject, SetDDrawObject method [DirectShow], SetDDrawObject method [DirectShow],IDDrawExclModeVideo interface, dshow.iddrawexclmodevideo_setddrawobject, strmif/IDDrawExclModeVideo::SetDDrawObject
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDDrawExclModeVideo::SetDDrawObject
 - strmif/IDDrawExclModeVideo::SetDDrawObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDDrawExclModeVideo.SetDDrawObject
---

# IDDrawExclModeVideo::SetDDrawObject


## -description

The <code>SetDDrawObject</code> method sets the DirectDraw object to be used in subsequent drawing.

## -parameters

### -param pDDrawObject [in]

Pointer to the <b>IDirectDraw</b> interface on the object to use.

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

A game application can use this method to share its DirectDraw object with the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter, so that the video can be drawn in a specified surface, as set in <a href="/windows/desktop/api/strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface">IDDrawExclModeVideo::SetDDrawSurface</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideo">IDDrawExclModeVideo Interface</a>