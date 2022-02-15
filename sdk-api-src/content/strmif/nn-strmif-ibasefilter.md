---
UID: NN:strmif.IBaseFilter
title: IBaseFilter (strmif.h)
description: The IBaseFilter interface is the primary interface for DirectShow filters.
helpviewer_keywords: ["IBaseFilter","IBaseFilter interface [DirectShow]","IBaseFilter interface [DirectShow]","described","IBaseFilterInterface","dshow.ibasefilter","strmif/IBaseFilter"]
old-location: dshow\ibasefilter.htm
tech.root: dshow
ms.assetid: d8c09dc7-dae8-4b51-8da8-69e64928a091
ms.date: 12/05/2018
ms.keywords: IBaseFilter, IBaseFilter interface [DirectShow], IBaseFilter interface [DirectShow],described, IBaseFilterInterface, dshow.ibasefilter, strmif/IBaseFilter
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
 - IBaseFilter
 - strmif/IBaseFilter
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
 - IBaseFilter
---

# IBaseFilter interface


## -description

The <code>IBaseFilter</code> interface is the primary interface for DirectShow filters. All DirectShow filters must expose this interface. The Filter Graph Manager uses this interface to control filters. Applications can use this interface to enumerate pins and query for filter information, but should not use it to change the state of a filter. Instead, use the <a href="/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl</a> interface on the Filter Graph Manager.

<b>Filter developers</b>: Implement this interface on every DirectShow filter. The <a href="/windows/desktop/DirectShow/cbasefilter">CBaseFilter</a> base class implements this interface.

## -inheritance

The <b>IBaseFilter</b> interface inherits from <a href="/windows/desktop/api/strmif/nn-strmif-imediafilter">IMediaFilter</a>. <b>IBaseFilter</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-imediafilter">IMediaFilter</a>
