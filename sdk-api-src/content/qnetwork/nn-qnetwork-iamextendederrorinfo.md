---
UID: NN:qnetwork.IAMExtendedErrorInfo
title: IAMExtendedErrorInfo (qnetwork.h)
description: The IAMExtendedErrorInfo interface is used to obtain error information. Note  This interface is not implemented by any default components in DirectShow. .
helpviewer_keywords: ["IAMExtendedErrorInfo","IAMExtendedErrorInfo interface [DirectShow]","IAMExtendedErrorInfo interface [DirectShow]","described","IAMExtendedErrorInfoInterface","dshow.iamextendederrorinfo","qnetwork/IAMExtendedErrorInfo"]
old-location: dshow\iamextendederrorinfo.htm
tech.root: dshow
ms.assetid: 0e3274e6-7c22-4175-8b2e-cdf4afc1225e
ms.date: 4/26/2023
ms.keywords: IAMExtendedErrorInfo, IAMExtendedErrorInfo interface [DirectShow], IAMExtendedErrorInfo interface [DirectShow],described, IAMExtendedErrorInfoInterface, dshow.iamextendederrorinfo, qnetwork/IAMExtendedErrorInfo
req.header: qnetwork.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMExtendedErrorInfo
 - qnetwork/IAMExtendedErrorInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMExtendedErrorInfo
---

# IAMExtendedErrorInfo interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMExtendedErrorInfo</code> interface is used to obtain error information. 


<div class="alert"><b>Note</b>  This interface is not implemented by any default components in DirectShow.</div>
<div> </div>

## -inheritance

The <b>IAMExtendedErrorInfo</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAMExtendedErrorInfo</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To define the interface identifier, include the header file Initguid.h before Qnetwork.h, but after Dshow.h and other header files:

<pre class="syntax" xml:space="preserve"><code>#include &lt;dshow.h&gt;
#include &lt;initguid.h&gt;
#include &lt;qnetwork.h&gt;
</code></pre>
<div class="alert"><b>Note</b>  Make sure that Initguid.h is included only once in your project. Otherwise, you will receive linker errors for duplicate GUID values.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
