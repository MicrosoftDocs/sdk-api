---
UID: NN:mfidl.IMFMediaTypeHandler
title: IMFMediaTypeHandler (mfidl.h)
description: Gets and sets media types on an object, such as a media source or media sink.
helpviewer_keywords: ["5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36","IMFMediaTypeHandler","IMFMediaTypeHandler interface [Media Foundation]","IMFMediaTypeHandler interface [Media Foundation]","described","mf.imfmediatypehandler","mfidl/IMFMediaTypeHandler"]
old-location: mf\imfmediatypehandler.htm
tech.root: mf
ms.assetid: 5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36
ms.date: 12/05/2018
ms.keywords: 5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36, IMFMediaTypeHandler, IMFMediaTypeHandler interface [Media Foundation], IMFMediaTypeHandler interface [Media Foundation],described, mf.imfmediatypehandler, mfidl/IMFMediaTypeHandler
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
 - IMFMediaTypeHandler
 - mfidl/IMFMediaTypeHandler
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
 - IMFMediaTypeHandler
---

# IMFMediaTypeHandler interface


## -description

Gets and sets media types on an object, such as a media source or media sink.

## -inheritance

The <b>IMFMediaTypeHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaTypeHandler</b> also has these types of members:

## -remarks

This interface is exposed by <i>media-type handlers</i>.

<ul>
<li> For media sources, get the media-type handler from the stream descriptor by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler">IMFStreamDescriptor::GetMediaTypeHandler</a>.</li>
<li>For media sinks, get the media-type handler by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-getmediatypehandler">IMFStreamSink::GetMediaTypeHandler</a>.</li>
</ul>
If you are implementing a custom media source or media sink, you can create a simple media-type handler by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatesimpletypehandler">MFCreateSimpleTypeHandler</a>, or you can provide your own implementation.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>



<a href="/windows/desktop/medfound/presentation-descriptors">Presentation Descriptors</a>
