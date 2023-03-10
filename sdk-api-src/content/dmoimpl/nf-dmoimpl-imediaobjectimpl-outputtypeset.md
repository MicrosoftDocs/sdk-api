---
UID: NF:dmoimpl.IMediaObjectImpl.OutputTypeSet
title: IMediaObjectImpl::OutputTypeSet (dmoimpl.h)
description: The OutputType method queries whether the media type was set on an output stream.
helpviewer_keywords: ["IMediaObjectImpl interface [DirectShow]","OutputTypeSet method","IMediaObjectImpl.OutputTypeSet","IMediaObjectImpl::OutputTypeSet","IMediaObjectImplOutputTypeSet","OutputTypeSet","OutputTypeSet method [DirectShow]","OutputTypeSet method [DirectShow]","IMediaObjectImpl interface","dmoimpl/IMediaObjectImpl::OutputTypeSet","dshow.imediaobjectimpl_outputtypeset"]
old-location: dshow\imediaobjectimpl_outputtypeset.htm
tech.root: dshow
ms.assetid: 4a2a2944-79ff-4173-b938-7b8a1203ec36
ms.date: 12/05/2018
ms.keywords: IMediaObjectImpl interface [DirectShow],OutputTypeSet method, IMediaObjectImpl.OutputTypeSet, IMediaObjectImpl::OutputTypeSet, IMediaObjectImplOutputTypeSet, OutputTypeSet, OutputTypeSet method [DirectShow], OutputTypeSet method [DirectShow],IMediaObjectImpl interface, dmoimpl/IMediaObjectImpl::OutputTypeSet, dshow.imediaobjectimpl_outputtypeset
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
 - IMediaObjectImpl::OutputTypeSet
 - dmoimpl/IMediaObjectImpl::OutputTypeSet
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
 - IMediaObjectImpl.OutputTypeSet
---

# IMediaObjectImpl::OutputTypeSet


## -description

The <code>OutputType</code> method queries whether the media type was set on an output stream.

## -parameters

### -param ulOutputStreamIndex

Index of an output stream.

## -returns

Returns <b>TRUE</b> if the media type was set on this stream, or <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/DirectShow/imediaobjectimpl-class-template">IMediaObjectImpl Class Template</a>