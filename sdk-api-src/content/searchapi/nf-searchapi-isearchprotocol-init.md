---
UID: NF:searchapi.ISearchProtocol.Init
title: ISearchProtocol::Init
author: windows-sdk-content
description: Initializes a protocol handler.
old-location: search\_search_ISearchProtocol_Init.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocol\init.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ISearchProtocol interface [search],Init method, ISearchProtocol.Init, ISearchProtocol::Init, Init, Init method [search], Init method [search],ISearchProtocol interface, _search_ISearchProtocol_Init, search._search_ISearchProtocol_Init, searchapi/ISearchProtocol::Init
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISearchProtocol::Init


## -description


Initializes a protocol handler. 
        


## -parameters




### -param pTimeoutInfo [in]

Type: <b><a href="https://msdn.microsoft.com/f6032470-abfd-4808-921c-7fa687ed640f">TIMEOUT_INFO</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/f6032470-abfd-4808-921c-7fa687ed640f">TIMEOUT_INFO</a> structure that contains information about connection time-outs. 
                


### -param pProtocolHandlerSite [in]

Type: <b><a href="https://msdn.microsoft.com/8fc14466-ffd3-4c96-9352-f33e01f95f8a">IProtocolHandlerSite</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/8fc14466-ffd3-4c96-9352-f33e01f95f8a">IProtocolHandlerSite</a> interface that enables protocol handlers to access <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFiltear</a>within the filter host. 
                


### -param pProxyInfo [in]

Type: <b><a href="https://msdn.microsoft.com/8e054fc6-10f0-45de-b89c-1ce6d489d707">PROXY_INFO</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/8e054fc6-10f0-45de-b89c-1ce6d489d707">PROXY_INFO</a> structure that contains information about the proxy settings necessary for accessing items in the content source.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After the protocol handler is <a href="7295a55b-12c7-4ed0-a7a4-9ecee16afdec">created</a>, this method is called to perform any initialization specific to the protocol handler. This method is not called again.  
      

Because the protocol host may unexpectedly terminate before calling <a href="https://msdn.microsoft.com/47f644a0-bd70-4af5-bf0b-5a6fe77cbefa">ISearchProtocol::ShutDown</a>, protocol handlers with persistent information, such as temporary files and registry entries, should do an initial clean-up of resources previously opened in this method before starting the current instance.
      



