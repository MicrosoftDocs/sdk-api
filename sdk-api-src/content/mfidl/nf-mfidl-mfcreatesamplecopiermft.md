---
UID: NF:mfidl.MFCreateSampleCopierMFT
title: MFCreateSampleCopierMFT function (mfidl.h)
description: Creates an instance of the sample copier transform.
helpviewer_keywords: ["MFCreateSampleCopierMFT","MFCreateSampleCopierMFT function [Media Foundation]","mf.mfcreatesamplecopiermft","mfidl/MFCreateSampleCopierMFT"]
old-location: mf\mfcreatesamplecopiermft.htm
tech.root: mf
ms.assetid: 4270c45e-4f20-4fcd-ad60-b205e334f692
ms.date: 12/05/2018
ms.keywords: MFCreateSampleCopierMFT, MFCreateSampleCopierMFT function [Media Foundation], mf.mfcreatesamplecopiermft, mfidl/MFCreateSampleCopierMFT
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateSampleCopierMFT
 - mfidl/MFCreateSampleCopierMFT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateSampleCopierMFT
---

# MFCreateSampleCopierMFT function


## -description

Creates an instance of the sample copier transform.

## -parameters

### -param ppCopierMFT [out]

Receives a pointer to the <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The sample copier is a Media Foundation transform (MFT) that copies data from input samples to output samples without modifying the data. The following data is copied from the sample:

<ul>
<li>All <a href="/windows/desktop/medfound/sample-attributes">Sample Attributes</a>.</li>
<li>The time stamp and duration.</li>
<li>Sample flags (see <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleflags">IMFSample::SetSampleFlags</a>).</li>
<li>The data in the media buffers. If the input sample contains multiple buffers, the data is copied into a single buffer on the output sample.</li>
</ul>
This MFT is useful in the following situation:

<ul>
<li>One pipeline object, such as a media source, allocates media samples for output.</li>
<li>Another pipeline object, such as a media sink, allocates its own media samples for input. For example, the object might require buffers allocated from a special memory pool, such as video memory.</li>
</ul>
The following diagram shows this situation with a media source and a media sink.

<img alt="Diagram: Media Source points to a Sample; Media Sink points to a second Sample; Sample Copier points to an arrow from the first sample to the second" src="./images/SampleCopierMFT.gif"/>

In order for the media sink to receive data from the media source, the data must be copied into the media samples owned by the media sink. The sample copier can be used for this purpose.

A specific example of such a media sink is the  <a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR). The EVR allocates samples that contain Direct3D surface buffers, so it cannot receive video samples directly from a media source. Starting in Windows 7, the topology loader automatically handles this case by inserting the sample copier between the media source and the EVR.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>