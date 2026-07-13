---
UID: NF:dmoimpl.IMediaObjectImpl.CheckTypesSet
title: IMediaObjectImpl::CheckTypesSet (dmoimpl.h)
description: The CheckTypesSet method determines whether the media type has been set on all of the streams.
helpviewer_keywords: ["CheckTypesSet","CheckTypesSet method [DirectShow]","CheckTypesSet method [DirectShow]","IMediaObjectImpl interface","IMediaObjectImpl interface [DirectShow]","CheckTypesSet method","IMediaObjectImpl.CheckTypesSet","IMediaObjectImpl::CheckTypesSet","IMediaObjectImplCheckTypesSet","dmoimpl/IMediaObjectImpl::CheckTypesSet","dshow.imediaobjectimpl_checktypesset"]
old-location: dshow\imediaobjectimpl_checktypesset.htm
tech.root: dshow
ms.assetid: 4dfbd638-00d6-410b-bf81-e343d7ca75d5
ms.date: 12/05/2018
ms.keywords: CheckTypesSet, CheckTypesSet method [DirectShow], CheckTypesSet method [DirectShow],IMediaObjectImpl interface, IMediaObjectImpl interface [DirectShow],CheckTypesSet method, IMediaObjectImpl.CheckTypesSet, IMediaObjectImpl::CheckTypesSet, IMediaObjectImplCheckTypesSet, dmoimpl/IMediaObjectImpl::CheckTypesSet, dshow.imediaobjectimpl_checktypesset
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
 - IMediaObjectImpl::CheckTypesSet
 - dmoimpl/IMediaObjectImpl::CheckTypesSet
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
 - IMediaObjectImpl.CheckTypesSet
---

# IMediaObjectImpl::CheckTypesSet


## -description

The <code>CheckTypesSet</code> method determines whether the media type has been set on all of the streams.



## -returns

Returns <b>TRUE</b> if the media type has been set on all of the non-optional streams. Otherwise, returns <b>FALSE</b>.

## -remarks

Call this method after any operation that changes the media type on a stream. This method sets a private flag within the class. Some <b>IMediaObjectImpl</b> methods test this flag to determine whether certain operations are permitted. These methods generally return DMO_E_TYPE_NOT_SET if the flag is <b>FALSE</b>.

The only two methods in <b>IMediaObject</b> that change the media type on a stream are <b>SetInputType</b> and <b>SetOutputType</b>. The class template implements both of these methods.

## -see-also

<a href="/windows/desktop/DirectShow/imediaobjectimpl-class-template">IMediaObjectImpl Class Template</a>
