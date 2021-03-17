---
UID: NF:dmoimpl.IMediaObjectImpl.InputType
title: IMediaObjectImpl::InputType (dmoimpl.h)
description: The InputType method retrieves the current media type for a specified input stream.
helpviewer_keywords: ["IMediaObjectImpl interface [DirectShow]","InputType method","IMediaObjectImpl.InputType","IMediaObjectImpl::InputType","IMediaObjectImplInputType","InputType","InputType method [DirectShow]","InputType method [DirectShow]","IMediaObjectImpl interface","dmoimpl/IMediaObjectImpl::InputType","dshow.imediaobjectimpl_inputtype"]
old-location: dshow\imediaobjectimpl_inputtype.htm
tech.root: dshow
ms.assetid: e595ac21-14e0-45ae-a286-7938ad0e0a02
ms.date: 12/05/2018
ms.keywords: IMediaObjectImpl interface [DirectShow],InputType method, IMediaObjectImpl.InputType, IMediaObjectImpl::InputType, IMediaObjectImplInputType, InputType, InputType method [DirectShow], InputType method [DirectShow],IMediaObjectImpl interface, dmoimpl/IMediaObjectImpl::InputType, dshow.imediaobjectimpl_inputtype
req.header: dmoimpl.h
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
req.lib: Dmoguids.lib; Msdmo.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaObjectImpl::InputType
 - dmoimpl/IMediaObjectImpl::InputType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
 - Msdmo.lib
 - Msdmo.dll
api_name:
 - IMediaObjectImpl.InputType
---

# IMediaObjectImpl::InputType


## -description

The <code>InputType</code> method retrieves the current media type for a specified input stream.

## -parameters

### -param ulInputStreamIndex

Index of an input stream.

## -returns

Returns a pointer to a <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type">DMO_MEDIA_TYPE</a> structure, or <b>NULL</b> if the media type is not set for this stream.

## -see-also

<a href="/windows/desktop/DirectShow/imediaobjectimpl-class-template">IMediaObjectImpl Class Template</a>