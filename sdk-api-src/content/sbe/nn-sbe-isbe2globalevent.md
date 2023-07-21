---
UID: NN:sbe.ISBE2GlobalEvent
title: ISBE2GlobalEvent (sbe.h)
description: Offers access to global spanning events and their data from the Stream Buffer Source filters. A global spanning event contains state information that applies to all the streams in a pipeline.
helpviewer_keywords: ["ISBE2GlobalEvent","ISBE2GlobalEvent interface [Microsoft TV Technologies]","ISBE2GlobalEvent interface [Microsoft TV Technologies]","described","mstv.isbe2globalevent","sbe/ISBE2GlobalEvent"]
old-location: mstv\isbe2globalevent.htm
tech.root: mstv
ms.assetid: 18bb9f8a-df97-468c-acb2-be7fa61a4789
ms.date: 12/05/2018
ms.keywords: ISBE2GlobalEvent, ISBE2GlobalEvent interface [Microsoft TV Technologies], ISBE2GlobalEvent interface [Microsoft TV Technologies],described, mstv.isbe2globalevent, sbe/ISBE2GlobalEvent
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
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
 - ISBE2GlobalEvent
 - sbe/ISBE2GlobalEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.h
api_name:
 - ISBE2GlobalEvent
---

# ISBE2GlobalEvent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Offers  access to global spanning events and their data from the <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filters.  A <i>global spanning event</i> contains state information that applies to all the streams in a pipeline.

## -inheritance

The <b>ISBE2GlobalEvent</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISBE2GlobalEvent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ISBE2GlobalEvent)</code>.
