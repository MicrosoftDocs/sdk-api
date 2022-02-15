---
UID: NN:mfidl.IMFStreamDescriptor
title: IMFStreamDescriptor (mfidl.h)
description: Gets information about one stream in a media source.
helpviewer_keywords: ["IMFStreamDescriptor","IMFStreamDescriptor interface [Media Foundation]","IMFStreamDescriptor interface [Media Foundation]","described","a076dc6e-d9cb-4f7e-8cc2-b66292da295f","mf.imfstreamdescriptor","mfidl/IMFStreamDescriptor"]
old-location: mf\imfstreamdescriptor.htm
tech.root: mf
ms.assetid: a076dc6e-d9cb-4f7e-8cc2-b66292da295f
ms.date: 12/05/2018
ms.keywords: IMFStreamDescriptor, IMFStreamDescriptor interface [Media Foundation], IMFStreamDescriptor interface [Media Foundation],described, a076dc6e-d9cb-4f7e-8cc2-b66292da295f, mf.imfstreamdescriptor, mfidl/IMFStreamDescriptor
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
 - IMFStreamDescriptor
 - mfidl/IMFStreamDescriptor
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
 - IMFStreamDescriptor
---

# IMFStreamDescriptor interface


## -description

Gets information about one stream in a media source.

## -inheritance

The <b>IMFStreamDescriptor</b> interface inherits from <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFStreamDescriptor</b> also has these types of members:

## -remarks

A presentation descriptor contains one or more stream descriptors. To get the stream descriptors from a presentation descriptor, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex">IMFPresentationDescriptor::GetStreamDescriptorByIndex</a>. To create a new stream descriptor, call <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor">MFCreateStreamDescriptor</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/presentation-descriptors">Presentation Descriptors</a>



<a href="/windows/desktop/medfound/stream-descriptor-attributes">Stream Descriptor Attributes</a>
