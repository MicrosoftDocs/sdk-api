---
UID: NN:control.IMediaPosition
title: IMediaPosition (control.h)
description: The IMediaPosition interface contains methods for seeking to a position within a stream.
helpviewer_keywords: ["IMediaPosition","IMediaPosition interface [DirectShow]","IMediaPosition interface [DirectShow]","described","IMediaPositionInterface","control/IMediaPosition","dshow.imediaposition"]
old-location: dshow\imediaposition.htm
tech.root: dshow
ms.assetid: 325dd9a4-80ca-43e3-9ff8-473df1b833e9
ms.date: 12/05/2018
ms.keywords: IMediaPosition, IMediaPosition interface [DirectShow], IMediaPosition interface [DirectShow],described, IMediaPositionInterface, control/IMediaPosition, dshow.imediaposition
req.header: control.h
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
 - IMediaPosition
 - control/IMediaPosition
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
 - IMediaPosition
---

# IMediaPosition interface


## -description

The <b>IMediaPosition</b> interface contains methods for seeking to a position within a stream. 


<div class="alert"><b>Note</b>  Applications should use <a href="/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking</a> instead of <b>IMediaPosition</b>. </div>
<div> </div>


This interface is exposed by the Filter Graph Manager as well as by individual filters. Applications should obtain an <b>IMediaPosition</b> interface pointer from the Filter Graph Manager, not from a filter. The Filter Graph Manager distributes method calls to all of the renderer filters. The renderer filters propagate the calls upstream to the source filters. This sequence of events ensures that all streams remain synchronized.

If one of the distributed calls returns an error, the Filter Graph Manager returns the first error value it received. Some of the distributed calls may have succeeded in this case. However, the filter graph does not return <b>E_NOTIMPL</b> unless all the distributed calls return <b>E_NOTIMPL</b>. If at least one filter in the graph implements the method, the Filter Graph Manager does not return <b>E_NOTIMPL</b>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaPosition</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMediaPosition</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
