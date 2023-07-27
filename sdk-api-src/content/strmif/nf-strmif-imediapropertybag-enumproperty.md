---
UID: NF:strmif.IMediaPropertyBag.EnumProperty
title: IMediaPropertyBag::EnumProperty (strmif.h)
description: The EnumProperty method retrieves a property/value pair.
helpviewer_keywords: ["EnumProperty","EnumProperty method [DirectShow]","EnumProperty method [DirectShow]","IMediaPropertyBag interface","IMediaPropertyBag interface [DirectShow]","EnumProperty method","IMediaPropertyBag.EnumProperty","IMediaPropertyBag::EnumProperty","IMediaPropertyBagEnumProperty","dshow.imediapropertybag_enumproperty","strmif/IMediaPropertyBag::EnumProperty"]
old-location: dshow\imediapropertybag_enumproperty.htm
tech.root: dshow
ms.assetid: 88cd9016-ef6f-467a-9e84-10b2ac578211
ms.date: 4/26/2023
ms.keywords: EnumProperty, EnumProperty method [DirectShow], EnumProperty method [DirectShow],IMediaPropertyBag interface, IMediaPropertyBag interface [DirectShow],EnumProperty method, IMediaPropertyBag.EnumProperty, IMediaPropertyBag::EnumProperty, IMediaPropertyBagEnumProperty, dshow.imediapropertybag_enumproperty, strmif/IMediaPropertyBag::EnumProperty
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
 - IMediaPropertyBag::EnumProperty
 - strmif/IMediaPropertyBag::EnumProperty
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
 - IMediaPropertyBag.EnumProperty
---

# IMediaPropertyBag::EnumProperty


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>EnumProperty</code> method retrieves a property/value pair.

## -parameters

### -param iProperty [in]

Index value of the pair.

### -param pvarPropertyName [in, out]

Pointer to a <b>VARIANT</b> that receives the property's name.

### -param pvarPropertyValue [in, out]

Pointer to a <b>VARIANT</b> that receives the property's value.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following:

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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_MORE_ITEMS)</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
</table>

## -remarks

The name is always a string. Set the variant type of the <i>pvarPropertyName</i> parameter to VT_EMPTY or VT_BSTR before calling this method.

The value can be a string (for INFO chunks) or an array of bytes (for DISP chunks). Set the variant type of the <i>pvarPropertyName</i> parameter to VT_EMPTY, VT_BSTR, or (VT_ARRAY | VT_UI1).

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediapropertybag">IMediaPropertyBag Interface</a>