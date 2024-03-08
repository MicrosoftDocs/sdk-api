---
UID: NN:sbe.ISBE2Crossbar
title: ISBE2Crossbar (sbe.h)
description: Defines crossbar functionality for a Stream Buffer Engine (SBE) version 2 (SBE2) Stream Buffer Source filter.
helpviewer_keywords: ["ISBE2Crossbar","ISBE2Crossbar interface [Microsoft TV Technologies]","ISBE2Crossbar interface [Microsoft TV Technologies]","described","mstv.isbe2crossbar","sbe/ISBE2Crossbar"]
old-location: mstv\isbe2crossbar.htm
tech.root: mstv
ms.assetid: 299816e7-2dad-44a5-a44d-9c3efe405d9b
ms.date: 12/05/2018
ms.keywords: ISBE2Crossbar, ISBE2Crossbar interface [Microsoft TV Technologies], ISBE2Crossbar interface [Microsoft TV Technologies],described, mstv.isbe2crossbar, sbe/ISBE2Crossbar
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
 - ISBE2Crossbar
 - sbe/ISBE2Crossbar
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
 - ISBE2Crossbar
---

# ISBE2Crossbar interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Defines crossbar functionality for a Stream Buffer Engine (SBE) version 2 (SBE2) <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter.

 A <i>crossbar</i> offers the following new features for the <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter in Windows 7:


<ul>
<li>It lets you predefine a collection of media streams that reside in a WTV file and map those streams to the filter's output pins. One of those collections is known as a <i>profile</i>, and a single mapping between a stream and an output pin is known as a <i>stream mapping</i>.</li>
<li>It lets you define which profile and which stream mappings to use for the filter when the media graph first starts running.</li>
<li>It lets you change the profile and stream mappings while the graph is running.</li>
</ul>


The <b>ISBE2Crossbar</b> interface is implemented by the <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter.

## -inheritance

The <b>ISBE2Crossbar</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISBE2Crossbar</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ISBE2Crossbar)</code>.
