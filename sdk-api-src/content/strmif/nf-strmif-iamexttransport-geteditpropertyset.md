---
UID: NF:strmif.IAMExtTransport.GetEditPropertySet
title: IAMExtTransport::GetEditPropertySet (strmif.h)
description: The GetEditPropertySet method retrieves the state of an edit event.
helpviewer_keywords: ["GetEditPropertySet","GetEditPropertySet method [DirectShow]","GetEditPropertySet method [DirectShow]","IAMExtTransport interface","IAMExtTransport interface [DirectShow]","GetEditPropertySet method","IAMExtTransport.GetEditPropertySet","IAMExtTransport::GetEditPropertySet","IAMExtTransportGetEditPropertySet","dshow.iamexttransport_geteditpropertyset","strmif/IAMExtTransport::GetEditPropertySet"]
old-location: dshow\iamexttransport_geteditpropertyset.htm
tech.root: dshow
ms.assetid: 1afb45da-947c-454d-8be9-46ac58802b9e
ms.date: 4/26/2023
ms.keywords: GetEditPropertySet, GetEditPropertySet method [DirectShow], GetEditPropertySet method [DirectShow],IAMExtTransport interface, IAMExtTransport interface [DirectShow],GetEditPropertySet method, IAMExtTransport.GetEditPropertySet, IAMExtTransport::GetEditPropertySet, IAMExtTransportGetEditPropertySet, dshow.iamexttransport_geteditpropertyset, strmif/IAMExtTransport::GetEditPropertySet
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
 - IAMExtTransport::GetEditPropertySet
 - strmif/IAMExtTransport::GetEditPropertySet
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
 - IAMExtTransport.GetEditPropertySet
---

# IAMExtTransport::GetEditPropertySet


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetEditPropertySet</code> method retrieves the state of an edit event.



This method is not implemented.

## -parameters

### -param EditID [in]

Specifies the edit property set. Use the identifier returned by the <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-seteditpropertyset">IAMExtTransport::SetEditPropertySet</a> method.

### -param pState [out]

Pointer to a <b>long</b> integer that receives the state of the edit property set:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_ACTIVE</td>
<td>The edit property set is active.</td>
</tr>
<tr>
<td>ED_DELETE</td>
<td>The edit property set was deleted.</td>
</tr>
<tr>
<td>ED_INACTIVE</td>
<td>The edit property set is inactive.</td>
</tr>
</table>

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-seteditpropertyset">IAMExtTransport::SetEditPropertySet</a>