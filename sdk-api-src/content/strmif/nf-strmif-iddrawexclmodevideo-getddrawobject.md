---
UID: NF:strmif.IDDrawExclModeVideo.GetDDrawObject
title: IDDrawExclModeVideo::GetDDrawObject (strmif.h)
description: The GetDDrawObject method retrieves the DirectDraw object being used by the Overlay Mixer filter.
helpviewer_keywords: ["GetDDrawObject","GetDDrawObject method [DirectShow]","GetDDrawObject method [DirectShow]","IDDrawExclModeVideo interface","IDDrawExclModeVideo interface [DirectShow]","GetDDrawObject method","IDDrawExclModeVideo.GetDDrawObject","IDDrawExclModeVideo::GetDDrawObject","IDDrawExclModeVideoGetDDrawObject","dshow.iddrawexclmodevideo_getddrawobject","strmif/IDDrawExclModeVideo::GetDDrawObject"]
old-location: dshow\iddrawexclmodevideo_getddrawobject.htm
tech.root: dshow
ms.assetid: b664fbcc-de14-42ca-95d0-97719e381605
ms.date: 12/05/2018
ms.keywords: GetDDrawObject, GetDDrawObject method [DirectShow], GetDDrawObject method [DirectShow],IDDrawExclModeVideo interface, IDDrawExclModeVideo interface [DirectShow],GetDDrawObject method, IDDrawExclModeVideo.GetDDrawObject, IDDrawExclModeVideo::GetDDrawObject, IDDrawExclModeVideoGetDDrawObject, dshow.iddrawexclmodevideo_getddrawobject, strmif/IDDrawExclModeVideo::GetDDrawObject
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
 - IDDrawExclModeVideo::GetDDrawObject
 - strmif/IDDrawExclModeVideo::GetDDrawObject
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
 - IDDrawExclModeVideo.GetDDrawObject
---

# IDDrawExclModeVideo::GetDDrawObject


## -description

The <code>GetDDrawObject</code> method retrieves the DirectDraw object being used by the Overlay Mixer filter.

## -parameters

### -param ppDDrawObject [out]

Address of a pointer to the <b>IDirectDraw</b> interface that the Overlay Mixer is using.

### -param pbUsingExternal [out]

Pointer to a variable that receives a Boolean value. It receives the value <b>TRUE</b> if the Overlay Mixer is using a DirectDraw object specified by <a href="/windows/desktop/api/strmif/nf-strmif-iddrawexclmodevideo-setddrawobject">IDDrawExclModeVideo::SetDDrawObject</a>, or <b>FALSE</b> otherwise.

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

If the filter graph has not set a DirectDraw object and the Overlay Mixer has not yet allocated one, then <i>pDDrawObject</i> will be set to <b>NULL</b> and <i>pbUsingExternal</i> will be set to <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideo">IDDrawExclModeVideo Interface</a>