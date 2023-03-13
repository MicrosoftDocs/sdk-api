---
UID: NF:docobj.IEnumOleDocumentViews.Reset
title: IEnumOleDocumentViews::Reset (docobj.h)
description: Resets the enumeration sequence to the beginning. (IEnumOleDocumentViews.Reset)
helpviewer_keywords: ["IEnumOleDocumentViews interface [COM]","Reset method","IEnumOleDocumentViews.Reset","IEnumOleDocumentViews::Reset","Reset","Reset method [COM]","Reset method [COM]","IEnumOleDocumentViews interface","_ole_ienumoledocumentviews_reset","com.ienumoledocumentviews_reset","docobj/IEnumOleDocumentViews::Reset"]
old-location: com\ienumoledocumentviews_reset.htm
tech.root: com
ms.assetid: b9dbdf36-fff1-4cd5-a890-219c8311dadf
ms.date: 12/05/2018
ms.keywords: IEnumOleDocumentViews interface [COM],Reset method, IEnumOleDocumentViews.Reset, IEnumOleDocumentViews::Reset, Reset, Reset method [COM], Reset method [COM],IEnumOleDocumentViews interface, _ole_ienumoledocumentviews_reset, com.ienumoledocumentviews_reset, docobj/IEnumOleDocumentViews::Reset
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
 - IEnumOleDocumentViews::Reset
 - docobj/IEnumOleDocumentViews::Reset
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
 - IEnumOleDocumentViews.Reset
---

# IEnumOleDocumentViews::Reset


## -description

Resets the enumeration sequence to the beginning.



## -returns

This method returns S_OK on success.

## -remarks

There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-ienumoledocumentviews">IEnumOleDocumentViews</a>
