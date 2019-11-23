---
UID: NN:sbe.ISBE2EnumStream
title: ISBE2EnumStream (sbe.h)

description: Enumerates a collection of streams. This is a utility interface, which you can use to enumerate the streams discovered in a WTV file. The Stream Buffer Source filter implements this interface.
old-location: mstv\isbe2enumstream.htm
tech.root: mstv
ms.assetid: 77a918f8-d305-4d4d-9a5c-523ddb796b26

ms.date: 12/05/2018
ms.keywords: ISBE2EnumStream, ISBE2EnumStream interface [Microsoft TV Technologies], ISBE2EnumStream interface [Microsoft TV Technologies],described, mstv.isbe2enumstream, sbe/ISBE2EnumStream
ms.topic: interface
f1_keywords: 
 - "sbe/ISBE2EnumStream"
dev_langs:
 - c++
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
req.dll: Sbe.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.dll
api_name:
 - ISBE2EnumStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISBE2EnumStream interface


## -description


Enumerates a collection of streams. This is a utility interface, which you can use to enumerate the streams discovered in a WTV file. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter implements this interface.

 To get a pointer to this interface,
<ol>
<li>Query the filter to get a pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2crossbar">ISBE2Crossbar</a> interface.</li>
<li>Call the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2crossbar-enumstreams">ISBE2Crossbar::EnumStreams</a> method, and take the value returned in the <i>ppstreams</i> output parameter.</li>
</ol>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISBE2EnumStream</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISBE2EnumStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISBE2EnumStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2enumstream-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2enumstream-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next <i>n</i> streams in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2enumstream-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2enumstream-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of streams in the enumeration sequence.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ISBE2EnumStream)</code>.



