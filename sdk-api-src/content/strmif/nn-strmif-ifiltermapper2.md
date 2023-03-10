---
UID: NN:strmif.IFilterMapper2
title: IFilterMapper2 (strmif.h)
description: Registers and unregisters filters, and locates filters in the registry.
helpviewer_keywords: ["IFilterMapper2","IFilterMapper2 interface [DirectShow]","IFilterMapper2 interface [DirectShow]","described","IFilterMapper2Interface","dshow.ifiltermapper2","strmif/IFilterMapper2"]
old-location: dshow\ifiltermapper2.htm
tech.root: dshow
ms.assetid: 6a3db838-cee3-4a9f-a924-fb55931acc83
ms.date: 12/05/2018
ms.keywords: IFilterMapper2, IFilterMapper2 interface [DirectShow], IFilterMapper2 interface [DirectShow],described, IFilterMapper2Interface, dshow.ifiltermapper2, strmif/IFilterMapper2
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFilterMapper2
 - strmif/IFilterMapper2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterMapper2
---

# IFilterMapper2 interface


## -description

Registers and unregisters filters, and locates filters in the registry. The <a href="/windows/desktop/DirectShow/filter-mapper">Filter Mapper</a> helper object implements this interface.

Filters use this interface to register and unregister themselves. When the filter graph manager builds a filter graph, it uses this interface to look up filters and determine their characteristics. Applications can also use this interface to look up filters. For more information, see <a href="/windows/desktop/DirectShow/using-the-filter-mapper">Using the Filter Mapper</a> and <a href="/windows/desktop/DirectShow/how-to-register-directshow-filters">How to Register DirectShow Filters</a>.

## -inheritance

The <b>IFilterMapper2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFilterMapper2</b> also has these types of members:

