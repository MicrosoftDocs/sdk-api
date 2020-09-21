---
UID: NN:structuredquery.IInterval
title: IInterval (structuredquery.h)
description: Provides a method to get the limits of an interval.
helpviewer_keywords: ["IInterval","IInterval interface [search]","IInterval interface [search]","described","_search_IInterval","search._search_IInterval","structuredquery/IInterval"]
old-location: search\_search_IInterval.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iinterval\iinterval.htm
ms.date: 12/05/2018
ms.keywords: IInterval, IInterval interface [search], IInterval interface [search],described, _search_IInterval, search._search_IInterval, structuredquery/IInterval
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IInterval
 - structuredquery/IInterval
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IInterval
---

# IInterval interface


## -description

Provides a method to get the limits of an interval.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInterval</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInterval</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInterval</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/structuredquery/nf-structuredquery-iinterval-getlimits">GetLimits</a>
</td>
<td align="left" width="63%">
Specifies the lower and upper limits of an interval, each of which may be infinite or a specific value.
        


When a condition tree expresses that the value of a property must fall in a certain range, the property can be expressed as a leaf node. The node must be a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> containing a <b>vt</b> value type tag of VT_UNKNOWN and an IUnknown* <b>punkVal</b> that is a pointer to an object that implements <b>IInterval</b>.

</td>
</tr>
</table>