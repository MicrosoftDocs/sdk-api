---
UID: NF:msrdc.ISimilarityTraitsMappedView.GetView
title: ISimilarityTraitsMappedView::GetView (msrdc.h)
description: Returns the beginning and ending addresses for the mapped view of a similarity traits table file.
helpviewer_keywords: ["GetView","GetView method [Remote Differential Compression]","GetView method [Remote Differential Compression]","ISimilarityTraitsMappedView interface","ISimilarityTraitsMappedView interface [Remote Differential Compression]","GetView method","ISimilarityTraitsMappedView.GetView","ISimilarityTraitsMappedView::GetView","fs.isimilaritytraitsmappedview_getview","msrdc/ISimilarityTraitsMappedView::GetView","rdc.isimilaritytraitsmappedview_getview"]
old-location: rdc\isimilaritytraitsmappedview_getview.htm
tech.root: rdc
ms.assetid: ac229f59-eb2f-471e-9f31-0e7139becdcb
ms.date: 12/05/2018
ms.keywords: GetView, GetView method [Remote Differential Compression], GetView method [Remote Differential Compression],ISimilarityTraitsMappedView interface, ISimilarityTraitsMappedView interface [Remote Differential Compression],GetView method, ISimilarityTraitsMappedView.GetView, ISimilarityTraitsMappedView::GetView, fs.isimilaritytraitsmappedview_getview, msrdc/ISimilarityTraitsMappedView::GetView, rdc.isimilaritytraitsmappedview_getview
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: MsRdc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISimilarityTraitsMappedView::GetView
 - msrdc/ISimilarityTraitsMappedView::GetView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarityTraitsMappedView.GetView
---

# ISimilarityTraitsMappedView::GetView


## -description

Returns the beginning and ending addresses for the mapped view of a similarity traits table file.

## -parameters

### -param mappedPageBegin [out]

Pointer to a location that receives the start of the data that is mapped for this view.

### -param mappedPageEnd [out]

Pointer to a location that receives the end of the data that is mapped for this view, plus one.

## -remarks

If there is no mapped view, then <code>*mappedPageBegin</code> must be set to zero. Otherwise, <code>*mappedPageBegin</code> is set to a valid pointer, and <code>*mappedPageBegin - *mappedPageEnd</code> equals the size, in bytes, of the mapped area.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmappedview">ISimilarityTraitsMappedView</a>