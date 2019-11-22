---
UID: NN:msxml.IXMLElementCollection
title: IXMLElementCollection (msxml.h)

description: Supports collection of XML elements for indexed access.
old-location: winprog\ixmlelementcollection.htm
tech.root: DevNotes
ms.assetid: 1d27e5fc-0491-44ee-9134-40f9f909b1cb

ms.date: 12/05/2018
ms.keywords: IXMLElementCollection, IXMLElementCollection interface [Windows API], IXMLElementCollection interface [Windows API],described, msxml/IXMLElementCollection, winprog.ixmlelementcollection
ms.topic: interface
f1_keywords: 
 - "msxml/IXMLElementCollection"
dev_langs:
 - c++
req.header: msxml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msxml.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Msxml.tlb
req.lib: 
req.dll: Msxml.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msxml.dll
api_name:
 - IXMLElementCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXMLElementCollection interface


## -description


The <b>IXMLElementCollection</b> interface supports collection of XML elements for indexed access.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXMLElementCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IXMLElementCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXMLElementCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msxml/nf-msxml-ixmlelementcollection-get_length">get_length</a>
</td>
<td align="left" width="63%">
Retrieves the number of elements in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msxml/nf-msxml-ixmlelementcollection-item">item</a>
</td>
<td align="left" width="63%">
Retrieves the child elements from a collection.

</td>
</tr>
</table> 

