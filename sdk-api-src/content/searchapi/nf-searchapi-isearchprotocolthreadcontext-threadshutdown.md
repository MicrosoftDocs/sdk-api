---
UID: NF:searchapi.ISearchProtocolThreadContext.ThreadShutdown
title: ISearchProtocolThreadContext::ThreadShutdown (searchapi.h)
description: Notifies the protocol handler that the thread is being shut down.
helpviewer_keywords: ["ISearchProtocolThreadContext interface [search]","ThreadShutdown method","ISearchProtocolThreadContext.ThreadShutdown","ISearchProtocolThreadContext::ThreadShutdown","ThreadShutdown","ThreadShutdown method [search]","ThreadShutdown method [search]","ISearchProtocolThreadContext interface","_search_ISearchProtocolThreadContext_ThreadShutdown","search._search_ISearchProtocolThreadContext_ThreadShutdown","searchapi/ISearchProtocolThreadContext::ThreadShutdown"]
old-location: search\_search_ISearchProtocolThreadContext_ThreadShutdown.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocolthreadcontext\threadshutdown.htm
ms.date: 12/05/2018
ms.keywords: ISearchProtocolThreadContext interface [search],ThreadShutdown method, ISearchProtocolThreadContext.ThreadShutdown, ISearchProtocolThreadContext::ThreadShutdown, ThreadShutdown, ThreadShutdown method [search], ThreadShutdown method [search],ISearchProtocolThreadContext interface, _search_ISearchProtocolThreadContext_ThreadShutdown, search._search_ISearchProtocolThreadContext_ThreadShutdown, searchapi/ISearchProtocolThreadContext::ThreadShutdown
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
 - ISearchProtocolThreadContext::ThreadShutdown
 - searchapi/ISearchProtocolThreadContext::ThreadShutdown
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
 - ISearchProtocolThreadContext.ThreadShutdown
---

# ISearchProtocolThreadContext::ThreadShutdown


## -description

Notifies the protocol handler that the thread is being shut down.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the protocol host is shut down, it calls this method as the last operation before terminating the filtering thread. Depending on the protocol handler, there might be some per-thread context, such as a logon session, that the protocol handler needs to clean up.

