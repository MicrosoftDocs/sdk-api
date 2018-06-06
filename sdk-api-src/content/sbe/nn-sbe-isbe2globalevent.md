---
UID: NN:sbe.ISBE2GlobalEvent
title: ISBE2GlobalEvent
author: windows-sdk-content
description: Offers access to global spanning events and their data from the Stream Buffer Source filters. A global spanning event contains state information that applies to all the streams in a pipeline.
old-location: mstv\isbe2globalevent.htm
old-project: mstv
ms.assetid: 18bb9f8a-df97-468c-acb2-be7fa61a4789
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ISBE2GlobalEvent, ISBE2GlobalEvent interface [Microsoft TV Technologies], ISBE2GlobalEvent interface [Microsoft TV Technologies],described, mstv.isbe2globalevent, sbe/ISBE2GlobalEvent
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.h
api_name:
 - ISBE2GlobalEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: Sbe.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISBE2GlobalEvent interface


## -description


Offers  access to global spanning events and their data from the <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filters.  A <i>global spanning event</i> contains state information that applies to all the streams in a pipeline.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISBE2GlobalEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISBE2GlobalEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISBE2GlobalEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ffa323d-6793-49e2-98ea-b9349c946c7c">GetEvent</a>
</td>
<td align="left" width="63%">
Gets an global spanning event and its data from a <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filter.


</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ISBE2GlobalEvent)</code>.



