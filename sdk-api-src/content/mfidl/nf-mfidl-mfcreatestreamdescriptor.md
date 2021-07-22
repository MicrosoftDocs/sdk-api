---
UID: NF:mfidl.MFCreateStreamDescriptor
title: MFCreateStreamDescriptor function (mfidl.h)
description: Creates a stream descriptor.
helpviewer_keywords: ["77a63d30-c03f-4339-9db3-eda60db9b194","MFCreateStreamDescriptor","MFCreateStreamDescriptor function [Media Foundation]","mf.mfcreatestreamdescriptor","mfidl/MFCreateStreamDescriptor"]
old-location: mf\mfcreatestreamdescriptor.htm
tech.root: mf
ms.assetid: 77a63d30-c03f-4339-9db3-eda60db9b194
ms.date: 12/05/2018
ms.keywords: 77a63d30-c03f-4339-9db3-eda60db9b194, MFCreateStreamDescriptor, MFCreateStreamDescriptor function [Media Foundation], mf.mfcreatestreamdescriptor, mfidl/MFCreateStreamDescriptor
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateStreamDescriptor
 - mfidl/MFCreateStreamDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateStreamDescriptor
---

# MFCreateStreamDescriptor function


## -description

Creates a stream descriptor.

## -parameters

### -param dwStreamIdentifier

Stream identifier.

### -param cMediaTypes

Number of elements in the <i>apMediaTypes</i> array.

### -param apMediaTypes

Pointer to an array of <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface pointers. These pointers are used to initialize the media type handler for the stream descriptor.

### -param ppDescriptor

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor">IMFStreamDescriptor</a> interface of the new stream descriptor. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If you are writing a custom media source, you can use this function to create stream descriptors for the source. This function automatically creates the stream descriptor media type handler and initializes it with the list of types given in <i>apMediaTypes</i>. The function does not set the current media type on the handler, however. To set the type, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype">IMFMediaTypeHandler::SetCurrentMediaType</a>.
      

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/presentation-descriptors">Presentation Descriptors</a>