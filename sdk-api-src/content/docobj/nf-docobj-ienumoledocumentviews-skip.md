---
UID: NF:docobj.IEnumOleDocumentViews.Skip
title: IEnumOleDocumentViews::Skip (docobj.h)
description: Skips over the specified number of items in the enumeration sequence. (IEnumOleDocumentViews.Skip)
helpviewer_keywords: ["IEnumOleDocumentViews interface [COM]","Skip method","IEnumOleDocumentViews.Skip","IEnumOleDocumentViews::Skip","Skip","Skip method [COM]","Skip method [COM]","IEnumOleDocumentViews interface","_ole_ienumoledocumentviews_skip","com.ienumoledocumentviews_skip","docobj/IEnumOleDocumentViews::Skip"]
old-location: com\ienumoledocumentviews_skip.htm
tech.root: com
ms.assetid: ea853e5a-ea73-441f-9b13-0425a4d734ad
ms.date: 12/05/2018
ms.keywords: IEnumOleDocumentViews interface [COM],Skip method, IEnumOleDocumentViews.Skip, IEnumOleDocumentViews::Skip, Skip, Skip method [COM], Skip method [COM],IEnumOleDocumentViews interface, _ole_ienumoledocumentviews_skip, com.ienumoledocumentviews_skip, docobj/IEnumOleDocumentViews::Skip
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
 - IEnumOleDocumentViews::Skip
 - docobj/IEnumOleDocumentViews::Skip
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
 - IEnumOleDocumentViews.Skip
---

# IEnumOleDocumentViews::Skip


## -description

Skips over the specified number of items in the enumeration sequence.

## -parameters

### -param cViews [in]

The number of items to be skipped.

## -returns

If the method skips the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-ienumoledocumentviews">IEnumOleDocumentViews</a>
