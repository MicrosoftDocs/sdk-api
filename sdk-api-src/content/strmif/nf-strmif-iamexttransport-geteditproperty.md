---
UID: NF:strmif.IAMExtTransport.GetEditProperty
title: IAMExtTransport::GetEditProperty (strmif.h)
description: The GetEditProperty method retrieves parameters and values associated with an edit event.
helpviewer_keywords: ["GetEditProperty","GetEditProperty method [DirectShow]","GetEditProperty method [DirectShow]","IAMExtTransport interface","IAMExtTransport interface [DirectShow]","GetEditProperty method","IAMExtTransport.GetEditProperty","IAMExtTransport::GetEditProperty","IAMExtTransportGetEditProperty","dshow.iamexttransport_geteditproperty","strmif/IAMExtTransport::GetEditProperty"]
old-location: dshow\iamexttransport_geteditproperty.htm
tech.root: dshow
ms.assetid: c36b1fb1-f0a7-49df-8a6c-fb90ab268b23
ms.date: 4/26/2023
ms.keywords: GetEditProperty, GetEditProperty method [DirectShow], GetEditProperty method [DirectShow],IAMExtTransport interface, IAMExtTransport interface [DirectShow],GetEditProperty method, IAMExtTransport.GetEditProperty, IAMExtTransport::GetEditProperty, IAMExtTransportGetEditProperty, dshow.iamexttransport_geteditproperty, strmif/IAMExtTransport::GetEditProperty
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
 - IAMExtTransport::GetEditProperty
 - strmif/IAMExtTransport::GetEditProperty
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
 - IAMExtTransport.GetEditProperty
---

# IAMExtTransport::GetEditProperty


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetEditProperty</code> method retrieves parameters and values associated with an edit event.



This method is not implemented.

## -parameters

### -param EditID [in]

Specifies the edit property set. Use the identifier returned by the <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-seteditpropertyset">IAMExtTransport::SetEditPropertySet</a> method.

### -param Param [in]

Specifies the edit event parameter to retrieve.

### -param pValue [out]

pointer to a variable that receives the parameter value.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

For a list of edit event parameters and their possible values, see <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-seteditproperty">IAMExtTransport::SetEditProperty</a>. In addition, this method supports ED_EDIT_TEST, which determines whether the device can perform the edit. If the device filter estimates that the device can perform the edit, it returns the value OATRUE in the <i>pValue</i> parameter. If not, it returns the value OAFALSE.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="/windows/desktop/DirectShow/msdv-driver">MSDV</a> does not support this method. It returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-seteditproperty">IAMExtTransport::SetEditProperty</a>