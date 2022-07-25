---
UID: NN:strmif.IEnumRegFilters
title: IEnumRegFilters (strmif.h)
description: Note  This interface has been deprecated.
helpviewer_keywords: ["IEnumRegFilters","IEnumRegFilters interface [DirectShow]","IEnumRegFilters interface [DirectShow]","described","IEnumRegFiltersInterface","dshow.ienumregfilters","strmif/IEnumRegFilters"]
old-location: dshow\ienumregfilters.htm
tech.root: dshow
ms.assetid: 59cb809d-84f5-42c4-a385-0f586af4d048
ms.date: 12/05/2018
ms.keywords: IEnumRegFilters, IEnumRegFilters interface [DirectShow], IEnumRegFilters interface [DirectShow],described, IEnumRegFiltersInterface, dshow.ienumregfilters, strmif/IEnumRegFilters
req.header: strmif.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumRegFilters
 - strmif/IEnumRegFilters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IEnumRegFilters
---

# IEnumRegFilters interface


## -description

<div class="alert"><b>Note</b>  This interface has been deprecated. New applications should call <a href="/windows/desktop/api/strmif/nf-strmif-ifiltermapper2-enummatchingfilters">IFilterMapper2::EnumMatchingFilters</a>, which enumerates monikers and returns a pointer to the <b>IEnumMoniker</b> interface.</div>
<div> </div>
This interface provides methods for enumerating registered filters. The <a href="/windows/desktop/api/strmif/nf-strmif-ifiltermapper-enummatchingfilters">IFilterMapper::EnumMatchingFilters</a> method returns a pointer to this interface. However, <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper">IFilterMapper</a> has been deprecated in favor of <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a>.

## -inheritance

The <b>IEnumRegFilters</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumRegFilters</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
