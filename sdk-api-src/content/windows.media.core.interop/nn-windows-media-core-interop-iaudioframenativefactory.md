---
UID: NN:windows.media.core.interop.IAudioFrameNativeFactory
title: IAudioFrameNativeFactory (windows.media.core.interop.h)
description: Creates instances of IAudioFrameNative.
helpviewer_keywords: ["IAudioFrameNativeFactory","IAudioFrameNativeFactory interface [Windows Runtime]","IAudioFrameNativeFactory interface [Windows Runtime]","described","windows/IAudioFrameNativeFactory","winrt.iaudioframenativefactory"]
old-location: winrt\iaudioframenativefactory.htm
tech.root: WinRT
ms.assetid: 8416020D-8CBA-4E70-B77C-55057E6212BA
ms.date: 12/05/2018
ms.keywords: IAudioFrameNativeFactory, IAudioFrameNativeFactory interface [Windows Runtime], IAudioFrameNativeFactory interface [Windows Runtime],described, windows/IAudioFrameNativeFactory, winrt.iaudioframenativefactory
req.header: windows.media.core.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IAudioFrameNativeFactory
 - windows.media.core.interop/IAudioFrameNativeFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.media.core.interop.h
api_name:
 - IAudioFrameNativeFactory
---

# IAudioFrameNativeFactory interface


## -description

Creates instances of <a href="/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative">IAudioFrameNative</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioFrameNativeFactory</b> interface inherits from <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>. <b>IAudioFrameNativeFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioFrameNativeFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/windows.media.core.interop/nf-windows-media-core-interop-iaudioframenativefactory-createfrommfsample">CreateFromMFSample</a>
</td>
<td align="left" width="63%">
Creates an <a href="/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative">IAudioFrameNative</a> from the provided <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>