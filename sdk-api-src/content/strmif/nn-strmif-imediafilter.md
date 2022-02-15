---
UID: NN:strmif.IMediaFilter
title: IMediaFilter (strmif.h)
description: The IMediaFilter interface controls the streaming state of a filter.All DirectShow filters implement this interface.
helpviewer_keywords: ["IMediaFilter","IMediaFilter interface [DirectShow]","IMediaFilter interface [DirectShow]","described","IMediaFilterInterface","dshow.imediafilter","strmif/IMediaFilter"]
old-location: dshow\imediafilter.htm
tech.root: dshow
ms.assetid: 5c0060e8-a9e5-4141-a38d-9a1bc55cc91b
ms.date: 12/05/2018
ms.keywords: IMediaFilter, IMediaFilter interface [DirectShow], IMediaFilter interface [DirectShow],described, IMediaFilterInterface, dshow.imediafilter, strmif/IMediaFilter
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
 - IMediaFilter
 - strmif/IMediaFilter
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
 - IMediaFilter
---

# IMediaFilter interface


## -description

The <code>IMediaFilter</code> interface controls the streaming state of a filter.

All DirectShow filters implement this interface. It provides methods for switching the filter between states (stopped, paused, and running); for retrieving the filter's current state; and for setting a reference clock. Applications should not call <code>IMediaFilter</code> methods on filters.

The <a href="/windows/desktop/DirectShow/filter-graph-manager">Filter Graph Manager</a> also exposes this interface. Applications can use the <b>SetSyncSource</b> method to set the graph reference clock, and <b>GetSyncSource</b> to retrieve the clock. Applications should not call the other methods on this interface. Instead, use the corresponding methods on the <a href="/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl</a> interface.

The <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface inherits from <code>IMediaFilter</code>.

## -inheritance

The <b>IMediaFilter</b> interface inherits from <b>IPersist</b>. <b>IMediaFilter</b> also has these types of members:

