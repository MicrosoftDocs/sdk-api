---
UID: NF:docobj.IEnumOleDocumentViews.Next
title: IEnumOleDocumentViews::Next (docobj.h)
description: Retrieves the specified number of items in the enumeration sequence. (IEnumOleDocumentViews.Next)
helpviewer_keywords: ["IEnumOleDocumentViews interface [COM]","Next method","IEnumOleDocumentViews.Next","IEnumOleDocumentViews::Next","Next","Next method [COM]","Next method [COM]","IEnumOleDocumentViews interface","com.ienumoledocumentviews_next","docobj/IEnumOleDocumentViews::Next"]
old-location: com\ienumoledocumentviews_next.htm
tech.root: com
ms.assetid: a58131bf-88ff-4661-9047-2d70b5e7931b
ms.date: 12/05/2018
ms.keywords: IEnumOleDocumentViews interface [COM],Next method, IEnumOleDocumentViews.Next, IEnumOleDocumentViews::Next, Next, Next method [COM], Next method [COM],IEnumOleDocumentViews interface, com.ienumoledocumentviews_next, docobj/IEnumOleDocumentViews::Next
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.Idl
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
 - IEnumOleDocumentViews::Next
 - docobj/IEnumOleDocumentViews::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IEnumOleDocumentViews.Next
---

# IEnumOleDocumentViews::Next


## -description

Retrieves the specified number of items in the enumeration sequence.

## -parameters

### -param cViews [in]

The number of items to be retrieved. If there are fewer than the requested number of items left in the sequence, this method retrieves the remaining elements.

If <i>pcFetched</i> is <b>NULL</b>, this parameter must be 1.

### -param rgpView [out]

An array of enumerated items.

The enumerator is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a>, and the caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> through each pointer enumerated. If <i>cViews</i> is greater than 1, the caller must also pass a non-<b>NULL</b> pointer passed to <i>pcFetched</i> to know how many pointers to release.

### -param pcFetched [in, out]

The number of items that were retrieved. This parameter is always less than or equal to the number of items requested. This parameter can be <b>NULL</b>, in which case the <i>cViews</i> parameter must be 1.

## -returns

If the method retrieves the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.

## -remarks

E_NOTIMPL is not allowed as a return value. If an error value is returned, no entries in the <i>rgpView</i> array are valid and no calls to Release are required.

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-ienumoledocumentviews">IEnumOleDocumentViews</a>



<a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a>
