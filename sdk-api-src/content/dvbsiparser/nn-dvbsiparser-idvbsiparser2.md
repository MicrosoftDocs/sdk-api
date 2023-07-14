---
UID: NN:dvbsiparser.IDvbSiParser2
title: IDvbSiParser2 (dvbsiparser.h)
description: The IDvbSiParser2 interface retrieves program specific information (PSI) and service information (SI) tables from a DVB transport stream.
helpviewer_keywords: ["IDvbSiParser2","IDvbSiParser2 interface [Microsoft TV Technologies]","IDvbSiParser2 interface [Microsoft TV Technologies]","described","dvbsiparser/IDvbSiParser2","mstv.idvbsiparser2"]
old-location: mstv\idvbsiparser2.htm
tech.root: mstv
ms.assetid: 085808e7-b067-470e-9edd-8795f4881485
ms.date: 12/05/2018
ms.keywords: IDvbSiParser2, IDvbSiParser2 interface [Microsoft TV Technologies], IDvbSiParser2 interface [Microsoft TV Technologies],described, dvbsiparser/IDvbSiParser2, mstv.idvbsiparser2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvbSiParser2
 - dvbsiparser/IDvbSiParser2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbSiParser2
---

# IDvbSiParser2 interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IDvbSiParser2</b> interface retrieves program specific information (PSI) and service information (SI) tables from a DVB transport stream.

## -inheritance

The <b>IDvbSiParser2</b> interface inherits from <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsiparser">IDvbSiParser</a>. <b>IDvbSiParser2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To get a pointer to this interface, call <b>CoCreateInstance</b>. Use the following CLSID:


```cpp
F6B96EDA-1A94-4476-A85F-4D3DC7B39C3F
```


This CLSID is not is not published in an SDK header; define a new GUID constant in your application.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsiparser">IDvbSiParser</a>
