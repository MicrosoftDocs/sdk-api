---
UID: NF:searchapi.ISearchProtocol.Init
title: ISearchProtocol::Init (searchapi.h)
description: Initializes a protocol handler.helpviewer_keywords: ["ISearchProtocol interface [search]","Init method","ISearchProtocol.Init","ISearchProtocol::Init","Init","Init method [search]","Init method [search]","ISearchProtocol interface","_search_ISearchProtocol_Init","search._search_ISearchProtocol_Init","searchapi/ISearchProtocol::Init"]
old-location: search\_search_ISearchProtocol_Init.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocol\init.htm
ms.date: 12/05/2018
ms.keywords: ISearchProtocol interface [search],Init method, ISearchProtocol.Init, ISearchProtocol::Init, Init, Init method [search], Init method [search],ISearchProtocol interface, _search_ISearchProtocol_Init, search._search_ISearchProtocol_Init, searchapi/ISearchProtocol::Init
f1_keywords:
- searchapi/ISearchProtocol.Init
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Searchapi.h
api_name:
- ISearchProtocol.Init
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchProtocol::Init


## -description


Initializes a protocol handler. 
        


## -parameters




### -param pTimeoutInfo [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/searchapi/ns-searchapi-timeout_info">TIMEOUT_INFO</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/ns-searchapi-timeout_info">TIMEOUT_INFO</a> structure that contains information about connection time-outs. 
                


### -param pProtocolHandlerSite [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iprotocolhandlersite">IProtocolHandlerSite</a>*</b>

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iprotocolhandlersite">IProtocolHandlerSite</a> interface that enables protocol handlers to access <a href="https://docs.microsoft.com/windows-hardware/test/hlk/api/ifilter-interface">IFiltear</a>within the filter host. 
                


### -param pProxyInfo [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/searchapi/ns-searchapi-proxy_info">PROXY_INFO</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/ns-searchapi-proxy_info">PROXY_INFO</a> structure that contains information about the proxy settings necessary for accessing items in the content source.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After the protocol handler is <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">created</a>, this method is called to perform any initialization specific to the protocol handler. This method is not called again.  
      

Because the protocol host may unexpectedly terminate before calling <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchprotocol-shutdown">ISearchProtocol::ShutDown</a>, protocol handlers with persistent information, such as temporary files and registry entries, should do an initial clean-up of resources previously opened in this method before starting the current instance.
      



