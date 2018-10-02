---
UID: NF:searchapi.ISearchProtocolThreadContext.ThreadIdle
title: ISearchProtocolThreadContext::ThreadIdle
author: windows-sdk-content
description: Notifies the protocol handler that the filtering thread is idle, so that the protocol handler can clean up any cache it might have built up.
old-location: search\_search_ISearchProtocolThreadContext_ThreadIdle.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocolthreadcontext\threadidle.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ISearchProtocolThreadContext interface [search],ThreadIdle method, ISearchProtocolThreadContext.ThreadIdle, ISearchProtocolThreadContext::ThreadIdle, ThreadIdle, ThreadIdle method [search], ThreadIdle method [search],ISearchProtocolThreadContext interface, _search_ISearchProtocolThreadContext_ThreadIdle, search._search_ISearchProtocolThreadContext_ThreadIdle, searchapi/ISearchProtocolThreadContext::ThreadIdle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchProtocolThreadContext.ThreadIdle
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISearchProtocolThreadContext::ThreadIdle


## -description


Notifies the protocol handler that the filtering thread is idle, so that the protocol handler can clean up any cache it might have built up.


## -parameters




### -param dwTimeElaspedSinceLastCallInMS [in]

Type: <b>DWORD</b>

Passes the idle time, in milliseconds, to the protocol handler.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called when the filtering thread is waiting for new requests from the indexer service so the protocol handler can use this idle time to clean up.



