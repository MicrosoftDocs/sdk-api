---
UID: NN:mfobjects.IMFSample
title: IMFSample (mfobjects.h)
description: Represents a media sample, which is a container object for media data.
helpviewer_keywords: ["IMFSample","IMFSample interface [Media Foundation]","IMFSample interface [Media Foundation]","described","b1c3758c-5133-41ee-b991-ae99d0296ccc","mf.imfsample","mfobjects/IMFSample"]
old-location: mf\imfsample.htm
tech.root: mf
ms.assetid: b1c3758c-5133-41ee-b991-ae99d0296ccc
ms.date: 12/05/2018
ms.keywords: IMFSample, IMFSample interface [Media Foundation], IMFSample interface [Media Foundation],described, b1c3758c-5133-41ee-b991-ae99d0296ccc, mf.imfsample, mfobjects/IMFSample
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSample
 - mfobjects/IMFSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSample
---

# IMFSample interface


## -description

Represents a media sample, which is a container object for media data. For video, a sample typically contains one video frame. For audio data, a sample typically contains multiple audio samples, rather than a single sample of audio.

A media sample contains zero or more buffers. Each buffer manages a block of memory, and is represented by the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface. A sample can have multiple buffers. The buffers are kept in an ordered list and accessed by index value. It is also valid to have an empty sample with no buffers.

## -inheritance

The <b>IMFSample</b> interface inherits from <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFSample</b> also has these types of members:

## -remarks

To create a new media sample, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample">MFCreateSample</a>.

<div class="alert"><b>Note</b>  <p class="note">When you call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems">CopyAllItems</a>, inherited from the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface, on an <b>IMFSample</b>, the sample time, duration, and flags are not copied to the destination sample. You must copy these values to the new sample manually.

</div>
<div> </div>
This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/media-samples">Media Samples</a>



<a href="/windows/desktop/medfound/sample-attributes">Sample Attributes</a>
