---
UID: NF:searchapi.ISearchProtocol.ShutDown
title: ISearchProtocol::ShutDown (searchapi.h)
description: Shuts down the protocol handler.
helpviewer_keywords: ["ISearchProtocol interface [search]","ShutDown method","ISearchProtocol.ShutDown","ISearchProtocol::ShutDown","ShutDown","ShutDown method [search]","ShutDown method [search]","ISearchProtocol interface","_search_ISearchProtocol_ShutDown","search._search_ISearchProtocol_ShutDown","searchapi/ISearchProtocol::ShutDown"]
old-location: search\_search_ISearchProtocol_ShutDown.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocol\shutdown.htm
ms.date: 12/05/2018
ms.keywords: ISearchProtocol interface [search],ShutDown method, ISearchProtocol.ShutDown, ISearchProtocol::ShutDown, ShutDown, ShutDown method [search], ShutDown method [search],ISearchProtocol interface, _search_ISearchProtocol_ShutDown, search._search_ISearchProtocol_ShutDown, searchapi/ISearchProtocol::ShutDown
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Srchprth.idl
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
 - ISearchProtocol::ShutDown
 - searchapi/ISearchProtocol::ShutDown
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
 - ISearchProtocol.ShutDown
---

# ISearchProtocol::ShutDown


## -description

Shuts down the protocol handler.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called by the protocol host to enable the protocol handler to clean up and release any associated resources.
          

The protocol host makes one call to this method before it exits. After this method is called, this instance will not be used any more. However, it is also possible for the protocol host process to terminate abruptly without calling this method. Protocol handlers that have persisted global states, such as registry entries and temporary files, should verify that those resources are cleaned up in the <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchprotocol-init">ISearchProtocol::Init</a> method before initialization.
