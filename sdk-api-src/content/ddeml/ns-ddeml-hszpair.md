---
UID: NS:ddeml.tagHSZPAIR
title: HSZPAIR (ddeml.h)
description: Contains a DDE service name and topic name. A DDE server application can use this structure during an XTYP_WILDCONNECT transaction to enumerate the service-topic pairs that it supports.
helpviewer_keywords: ["*PHSZPAIR","HSZPAIR","HSZPAIR structure [Data Exchange]","PHSZPAIR","PHSZPAIR structure pointer [Data Exchange]","_win32_HSZPAIR_str","_win32_hszpair_str_cpp","dataxchg.hszpair","ddeml/HSZPAIR","ddeml/PHSZPAIR","winui._win32_hszpair_str"]
old-location: dataxchg\hszpair.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange\dynamicdataexchangereference\dynamicdataexchangestructures\hszpair.htm
ms.date: 12/05/2018
ms.keywords: '*PHSZPAIR, HSZPAIR, HSZPAIR structure [Data Exchange], PHSZPAIR, PHSZPAIR structure pointer [Data Exchange], _win32_HSZPAIR_str, _win32_hszpair_str_cpp, dataxchg.hszpair, ddeml/HSZPAIR, ddeml/PHSZPAIR, winui._win32_hszpair_str'
req.header: ddeml.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: HSZPAIR, *PHSZPAIR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHSZPAIR
 - ddeml/tagHSZPAIR
 - PHSZPAIR
 - ddeml/PHSZPAIR
 - HSZPAIR
 - ddeml/HSZPAIR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ddeml.h
api_name:
 - HSZPAIR
---

# HSZPAIR structure


## -description

Contains a DDE service name and topic name. A DDE server application can use this structure during an <a href="/windows/desktop/dataxchg/xtyp-wildconnect">XTYP_WILDCONNECT</a> transaction to enumerate the service-topic pairs that it supports.

## -struct-fields

### -field hszSvc

Type: <b>HSZ</b>

A handle to the service name.

### -field hszTopic

Type: <b>HSZ</b>

A handle to the topic name.

## -see-also

<a href="/windows/desktop/dataxchg/about-dynamic-data-exchange">About Dynamic Data Exchange</a>