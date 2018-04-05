---
UID: NN:sbe.ISBE2EnumStream
title: ISBE2EnumStream
author: windows-driver-content
description: Enumerates a collection of streams. This is a utility interface, which you can use to enumerate the streams discovered in a WTV file. The Stream Buffer Source filter implements this interface.
old-location: mstv\isbe2enumstream.htm
old-project: mstv
ms.assetid: 77a918f8-d305-4d4d-9a5c-523ddb796b26
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ISBE2EnumStream, ISBE2EnumStream interface [Microsoft TV Technologies], ISBE2EnumStream interface [Microsoft TV Technologies], described, mstv.isbe2enumstream, sbe/ISBE2EnumStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sbe.dll
api_name:
-	ISBE2EnumStream
product: Windows
targetos: Windows
req.lib: 
req.dll: Sbe.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ISBE2EnumStream interface


## -description


Enumerates a collection of streams. This is a utility interface, which you can use to enumerate the streams discovered in a WTV file. The <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filter implements this interface.

 To get a pointer to this interface,
<ol>
<li>Query the filter to get a pointer to the <a href="https://msdn.microsoft.com/299816e7-2dad-44a5-a44d-9c3efe405d9b">ISBE2Crossbar</a> interface.</li>
<li>Call the  <a href="https://msdn.microsoft.com/891dc676-8930-41bc-a0ae-4a080c6d4cd6">ISBE2Crossbar::EnumStreams</a> method, and take the value returned in the <i>ppstreams</i> output parameter.</li>
</ol>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISBE2EnumStream</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISBE2EnumStream</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next <i>n</i> streams in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of streams in the enumeration sequence.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ISBE2EnumStream)</code>.



