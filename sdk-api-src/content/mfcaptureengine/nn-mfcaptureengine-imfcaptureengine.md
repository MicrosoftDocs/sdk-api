---
UID: NN:mfcaptureengine.IMFCaptureEngine
title: IMFCaptureEngine (mfcaptureengine.h)
description: Controls one or more capture devices.
helpviewer_keywords: ["IMFCaptureEngine","IMFCaptureEngine interface [Media Foundation]","IMFCaptureEngine interface [Media Foundation]","described","mf.imfcaptureengine","mfcaptureengine/IMFCaptureEngine"]
old-location: mf\imfcaptureengine.htm
tech.root: mf
ms.assetid: 4A2A0536-4255-40AB-BCAB-228B09343583
ms.date: 12/05/2018
ms.keywords: IMFCaptureEngine, IMFCaptureEngine interface [Media Foundation], IMFCaptureEngine interface [Media Foundation],described, mf.imfcaptureengine, mfcaptureengine/IMFCaptureEngine
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IMFCaptureEngine
 - mfcaptureengine/IMFCaptureEngine
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureEngine
---

# IMFCaptureEngine interface


## -description

Controls one or more capture devices. The capture engine implements this interface. To get a pointer to this interface, call either <a href="https://docs.microsoft.com/windows/desktop/medfound/mfcreatecaptureengine">MFCreateCaptureEngine</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineclassfactory-createinstance">IMFCaptureEngineClassFactory::CreateInstance</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCaptureEngine</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFCaptureEngine</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFCaptureEngine</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-getsink">GetSink</a>
</td>
<td align="left" width="63%">
Gets a pointer to one of the capture sink objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-getsource">GetSource</a>
</td>
<td align="left" width="63%">
Gets a pointer to the capture source object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the capture engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-startpreview">StartPreview</a>
</td>
<td align="left" width="63%">
Starts preview.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-startrecord">StartRecord</a>
</td>
<td align="left" width="63%">
Starts recording audio and/or video to a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-stoppreview">StopPreview</a>
</td>
<td align="left" width="63%">
Stops preview.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-stoprecord">StopRecord</a>
</td>
<td align="left" width="63%">
Stops recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-takephoto">TakePhoto</a>
</td>
<td align="left" width="63%">
Captures a still image from the video stream.

</td>
</tr>
</table>

## -remarks

<b>IMFCaptureEngine</b> only supports one pass CBR encoding.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>

