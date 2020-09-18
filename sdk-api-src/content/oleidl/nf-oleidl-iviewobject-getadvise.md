---
UID: NF:oleidl.IViewObject.GetAdvise
title: IViewObject::GetAdvise (oleidl.h)
description: Retrieves the advisory connection on the object that was used in the most recent call to IViewObject::SetAdvise.
helpviewer_keywords: ["GetAdvise","GetAdvise method [COM]","GetAdvise method [COM]","IViewObject interface","IViewObject interface [COM]","GetAdvise method","IViewObject.GetAdvise","IViewObject::GetAdvise","_ole_iviewobject_getadvise","com.iviewobject_getadvise","oleidl/IViewObject::GetAdvise"]
old-location: com\iviewobject_getadvise.htm
tech.root: com
ms.assetid: c56f6cbb-d2ea-4db4-a660-db8b7540ac94
ms.date: 12/05/2018
ms.keywords: GetAdvise, GetAdvise method [COM], GetAdvise method [COM],IViewObject interface, IViewObject interface [COM],GetAdvise method, IViewObject.GetAdvise, IViewObject::GetAdvise, _ole_iviewobject_getadvise, com.iviewobject_getadvise, oleidl/IViewObject::GetAdvise
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IViewObject::GetAdvise
 - oleidl/IViewObject::GetAdvise
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IViewObject.GetAdvise
---

# IViewObject::GetAdvise


## -description

Retrieves the advisory connection on the object that was used in the most recent call to <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-setadvise">IViewObject::SetAdvise</a>.

## -parameters

### -param pAspects [out]

Pointer to where the <i>dwAspect</i> parameter from the previous <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-setadvise">IViewObject::SetAdvise</a> call is returned. If this pointer is <b>NULL</b>, the caller does not permit this value to be returned.

### -param pAdvf [out]

Pointer to where the <i>advf</i> parameter from the previous <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-setadvise">IViewObject::SetAdvise</a> call is returned. If this pointer is <b>NULL</b>, the caller does not permit this value to be returned.

### -param ppAdvSink [out]

Address of <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> pointer variable that receives the interface pointer to the advise sink. The connection to this advise sink must have been established with a previous <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-setadvise">IViewObject::SetAdvise</a> call, which provides the <i>pAdvSink</i> parameter. If <i>ppvAdvSink</i> is <b>NULL</b>, there is no established advisory connection.

## -returns

This method returns S_OK on success.

## -see-also

<a href="/windows/desktop/api/objidl/ne-objidl-advf">ADVF</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-setadvise">IViewObject::SetAdvise</a>