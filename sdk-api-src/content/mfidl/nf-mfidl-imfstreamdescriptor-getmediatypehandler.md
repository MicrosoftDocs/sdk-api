---
UID: NF:mfidl.IMFStreamDescriptor.GetMediaTypeHandler
title: IMFStreamDescriptor::GetMediaTypeHandler (mfidl.h)
description: Retrieves a media type handler for the stream. The media type handler can be used to enumerate supported media types for the stream, get the current media type, and set the media type.
helpviewer_keywords: ["8e991417-fe15-4749-94c4-26c621692b52","GetMediaTypeHandler","GetMediaTypeHandler method [Media Foundation]","GetMediaTypeHandler method [Media Foundation]","IMFStreamDescriptor interface","IMFStreamDescriptor interface [Media Foundation]","GetMediaTypeHandler method","IMFStreamDescriptor.GetMediaTypeHandler","IMFStreamDescriptor::GetMediaTypeHandler","mf.imfstreamdescriptor_getmediatypehandler","mfidl/IMFStreamDescriptor::GetMediaTypeHandler"]
old-location: mf\imfstreamdescriptor_getmediatypehandler.htm
tech.root: mf
ms.assetid: 8e991417-fe15-4749-94c4-26c621692b52
ms.date: 12/05/2018
ms.keywords: 8e991417-fe15-4749-94c4-26c621692b52, GetMediaTypeHandler, GetMediaTypeHandler method [Media Foundation], GetMediaTypeHandler method [Media Foundation],IMFStreamDescriptor interface, IMFStreamDescriptor interface [Media Foundation],GetMediaTypeHandler method, IMFStreamDescriptor.GetMediaTypeHandler, IMFStreamDescriptor::GetMediaTypeHandler, mf.imfstreamdescriptor_getmediatypehandler, mfidl/IMFStreamDescriptor::GetMediaTypeHandler
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
 - IMFStreamDescriptor::GetMediaTypeHandler
 - mfidl/IMFStreamDescriptor::GetMediaTypeHandler
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
 - IMFStreamDescriptor.GetMediaTypeHandler
---

# IMFStreamDescriptor::GetMediaTypeHandler


## -description

Retrieves a media type handler for the stream. The media type handler can be used to enumerate supported media types for the stream, get the current media type, and set the media type.

## -parameters

### -param ppMediaTypeHandler [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler">IMFMediaTypeHandler</a> interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor">IMFStreamDescriptor</a>



<a href="/windows/desktop/medfound/presentation-descriptors">Presentation Descriptors</a>