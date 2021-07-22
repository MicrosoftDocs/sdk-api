---
UID: NN:mfidl.IMFPresentationDescriptor
title: IMFPresentationDescriptor (mfidl.h)
description: Describes the details of a presentation. A presentation is a set of related media streams that share a common presentation time.
helpviewer_keywords: ["IMFPresentationDescriptor","IMFPresentationDescriptor interface [Media Foundation]","IMFPresentationDescriptor interface [Media Foundation]","described","db03e212-7021-433e-84dc-410b2cf7af87","mf.imfpresentationdescriptor","mfidl/IMFPresentationDescriptor"]
old-location: mf\imfpresentationdescriptor.htm
tech.root: mf
ms.assetid: db03e212-7021-433e-84dc-410b2cf7af87
ms.date: 12/05/2018
ms.keywords: IMFPresentationDescriptor, IMFPresentationDescriptor interface [Media Foundation], IMFPresentationDescriptor interface [Media Foundation],described, db03e212-7021-433e-84dc-410b2cf7af87, mf.imfpresentationdescriptor, mfidl/IMFPresentationDescriptor
req.header: mfidl.h
req.include-header: 
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
 - IMFPresentationDescriptor
 - mfidl/IMFPresentationDescriptor
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
 - IMFPresentationDescriptor
---

# IMFPresentationDescriptor interface


## -description

Describes the details of a presentation. A <i>presentation</i> is a set of related media streams that share a common presentation time.

## -inheritance

The <b>IMFPresentationDescriptor</b> interface inherits from <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFPresentationDescriptor</b> also has these types of members:

## -remarks

Presentation descriptors are used to configure media sources and some media sinks. To get the presentation descriptor from a media source, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor">IMFMediaSource::CreatePresentationDescriptor</a>. To create a new presentation descriptor, call <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor">MFCreatePresentationDescriptor</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/presentation-descriptor-attributes">Presentation Descriptor Attributes</a>



<a href="/windows/desktop/medfound/presentation-descriptors">Presentation Descriptors</a>
