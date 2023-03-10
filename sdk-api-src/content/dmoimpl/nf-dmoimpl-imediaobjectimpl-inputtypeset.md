---
UID: NF:dmoimpl.IMediaObjectImpl.InputTypeSet
title: IMediaObjectImpl::InputTypeSet (dmoimpl.h)
description: The InputTypeSet method queries whether the media type was set on an input stream.
helpviewer_keywords: ["IMediaObjectImpl interface [DirectShow]","InputTypeSet method","IMediaObjectImpl.InputTypeSet","IMediaObjectImpl::InputTypeSet","IMediaObjectImplInputTypeSet","InputTypeSet","InputTypeSet method [DirectShow]","InputTypeSet method [DirectShow]","IMediaObjectImpl interface","dmoimpl/IMediaObjectImpl::InputTypeSet","dshow.imediaobjectimpl_inputtypeset"]
old-location: dshow\imediaobjectimpl_inputtypeset.htm
tech.root: dshow
ms.assetid: f7f2f594-31ed-4c75-8221-9c62f8b4bed3
ms.date: 12/05/2018
ms.keywords: IMediaObjectImpl interface [DirectShow],InputTypeSet method, IMediaObjectImpl.InputTypeSet, IMediaObjectImpl::InputTypeSet, IMediaObjectImplInputTypeSet, InputTypeSet, InputTypeSet method [DirectShow], InputTypeSet method [DirectShow],IMediaObjectImpl interface, dmoimpl/IMediaObjectImpl::InputTypeSet, dshow.imediaobjectimpl_inputtypeset
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
 - IMediaObjectImpl::InputTypeSet
 - dmoimpl/IMediaObjectImpl::InputTypeSet
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
 - IMediaObjectImpl.InputTypeSet
---

# IMediaObjectImpl::InputTypeSet


## -description

The <code>InputTypeSet</code> method queries whether the media type was set on an input stream.

## -parameters

### -param ulInputStreamIndex

Index of an input stream.

## -returns

Returns <b>TRUE</b> if the media type was set on this stream, or <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/DirectShow/imediaobjectimpl-class-template">IMediaObjectImpl Class Template</a>