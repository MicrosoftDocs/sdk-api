---
UID: NF:mfidl.MFCreateSampleGrabberSinkActivate
title: MFCreateSampleGrabberSinkActivate function (mfidl.h)
description: Creates an activation object for the sample grabber media sink.
helpviewer_keywords: ["MFCreateSampleGrabberSinkActivate","MFCreateSampleGrabberSinkActivate function [Media Foundation]","ac8e415e-5df8-4fdb-adf6-c3c717c3d625","mf.mfcreatesamplegrabbersinkactivate","mfidl/MFCreateSampleGrabberSinkActivate"]
old-location: mf\mfcreatesamplegrabbersinkactivate.htm
tech.root: mf
ms.assetid: ac8e415e-5df8-4fdb-adf6-c3c717c3d625
ms.date: 12/05/2018
ms.keywords: MFCreateSampleGrabberSinkActivate, MFCreateSampleGrabberSinkActivate function [Media Foundation], ac8e415e-5df8-4fdb-adf6-c3c717c3d625, mf.mfcreatesamplegrabbersinkactivate, mfidl/MFCreateSampleGrabberSinkActivate
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - MFCreateSampleGrabberSinkActivate
 - mfidl/MFCreateSampleGrabberSinkActivate
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
 - MFCreateSampleGrabberSinkActivate
---

# MFCreateSampleGrabberSinkActivate function


## -description

Creates an activation object for the sample grabber media sink.

## -parameters

### -param pIMFMediaType

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface, defining the media type for the sample grabber's input stream.

### -param pIMFSampleGrabberSinkCallback

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback">IMFSampleGrabberSinkCallback</a> interface of a callback object. The caller must implement this interface.

### -param ppIActivate

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface. Use this interface to complete the creation of the sample grabber. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To create the sample grabber sink, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a> on the pointer received in the <i>ppIActivate</i> parameter.

Before calling <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">ActivateObject</a>, you can configure the sample grabber by setting any of the following attributes on the <i>ppIActivate</i> pointer:

<ul>
<li>
<a href="/windows/desktop/medfound/mf-samplegrabbersink-ignore-clock">MF_SAMPLEGRABBERSINK_IGNORE_CLOCK</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-samplegrabbersink-sample-time-offset-attribute">MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>