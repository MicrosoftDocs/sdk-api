---
UID: NN:searchapi.ISearchProtocolThreadContext
title: ISearchProtocolThreadContext (searchapi.h)
description: This optional interface enables the protocol handler to perform an action on the thread used for filtering in the protocol host.
helpviewer_keywords: ["ISearchProtocolThreadContext","ISearchProtocolThreadContext interface [search]","ISearchProtocolThreadContext interface [search]","described","_search_ISearchProtocolThreadContext","search._search_ISearchProtocolThreadContext","searchapi/ISearchProtocolThreadContext"]
old-location: search\_search_ISearchProtocolThreadContext.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocolthreadcontext\isearchprotocolthreadcontext.htm
ms.date: 12/05/2018
ms.keywords: ISearchProtocolThreadContext, ISearchProtocolThreadContext interface [search], ISearchProtocolThreadContext interface [search],described, _search_ISearchProtocolThreadContext, search._search_ISearchProtocolThreadContext, searchapi/ISearchProtocolThreadContext
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
 - ISearchProtocolThreadContext
 - searchapi/ISearchProtocolThreadContext
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
 - ISearchProtocolThreadContext
---

# ISearchProtocolThreadContext interface


## -description

This optional interface enables the protocol handler to perform an action on the thread used for filtering in the protocol host. When the protocol host starts, it first initializes all the protocol handlers, and then it creates the filtering thread(s). The methods on this interface enable protocol handlers to manage their resources that are used by a filtering thread.

## -inheritance

The <b>ISearchProtocolThreadContext</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchProtocolThreadContext</b> also has these types of members:

