---
UID: NN:dvbsiparser.IDvbSiParser2
title: IDvbSiParser2 (dvbsiparser.h)
description: The IDvbSiParser2 interface retrieves program specific information (PSI) and service information (SI) tables from a DVB transport stream.
old-location: mstv\idvbsiparser2.htm
tech.root: mstv
ms.assetid: 085808e7-b067-470e-9edd-8795f4881485
ms.date: 12/05/2018
ms.keywords: IDvbSiParser2, IDvbSiParser2 interface [Microsoft TV Technologies], IDvbSiParser2 interface [Microsoft TV Technologies],described, dvbsiparser/IDvbSiParser2, mstv.idvbsiparser2
ms.topic: interface
f1_keywords:
- dvbsiparser/IDvbSiParser2
dev_langs:
- c++
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IDvbSiParser2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbSiParser2 interface


## -description



The <b>IDvbSiParser2</b> interface retrieves program specific information (PSI) and service information (SI) tables from a DVB transport stream.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbSiParser2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsiparser">IDvbSiParser</a>. <b>IDvbSiParser2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbSiParser2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser2-geteit2">GetEIT2</a>
</td>
<td align="left" width="63%">
Gets the event information table (EIT).

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <b>CoCreateInstance</b>. Use the following CLSID:


```cpp
F6B96EDA-1A94-4476-A85F-4D3DC7B39C3F
```


This CLSID is not is not published in an SDK header; define a new GUID constant in your application.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsiparser">IDvbSiParser</a>
 

 

