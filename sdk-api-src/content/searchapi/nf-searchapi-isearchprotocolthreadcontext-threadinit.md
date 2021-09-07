---
UID: NF:searchapi.ISearchProtocolThreadContext.ThreadInit
title: ISearchProtocolThreadContext::ThreadInit (searchapi.h)
description: Initializes communication between the protocol handler and the protocol host.
helpviewer_keywords: ["ISearchProtocolThreadContext interface [search]","ThreadInit method","ISearchProtocolThreadContext.ThreadInit","ISearchProtocolThreadContext::ThreadInit","ThreadInit","ThreadInit method [search]","ThreadInit method [search]","ISearchProtocolThreadContext interface","_search_ISearchProtocolThreadContext_ThreadInit","search._search_ISearchProtocolThreadContext_ThreadInit","searchapi/ISearchProtocolThreadContext::ThreadInit"]
old-location: search\_search_ISearchProtocolThreadContext_ThreadInit.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocolthreadcontext\threadinit.htm
ms.date: 12/05/2018
ms.keywords: ISearchProtocolThreadContext interface [search],ThreadInit method, ISearchProtocolThreadContext.ThreadInit, ISearchProtocolThreadContext::ThreadInit, ThreadInit, ThreadInit method [search], ThreadInit method [search],ISearchProtocolThreadContext interface, _search_ISearchProtocolThreadContext_ThreadInit, search._search_ISearchProtocolThreadContext_ThreadInit, searchapi/ISearchProtocolThreadContext::ThreadInit
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Urlacc.idl
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
 - ISearchProtocolThreadContext::ThreadInit
 - searchapi/ISearchProtocolThreadContext::ThreadInit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchProtocolThreadContext.ThreadInit
---

# ISearchProtocolThreadContext::ThreadInit


## -description

Initializes communication between the protocol handler and the protocol host.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After being created by the protocol host, a thread calls this method on the protocol handler to initialize communication between the protocol handler and its host. Depending on the protocol handler, the host might need to provide some per-thread context (for example, a logon session).

