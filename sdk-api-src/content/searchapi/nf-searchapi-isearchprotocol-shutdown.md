---
UID: NF:searchapi.ISearchProtocol.ShutDown
title: ISearchProtocol::ShutDown method
author: windows-driver-content
description: Shuts down the protocol handler.
old-location: search\_search_ISearchProtocol_ShutDown.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocol\shutdown.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ISearchProtocol, ISearchProtocol interface [search], ShutDown method, ISearchProtocol::ShutDown, ShutDown method [search], ShutDown method [search], ISearchProtocol interface, ShutDown,ISearchProtocol.ShutDown, _search_ISearchProtocol_ShutDown, search._search_ISearchProtocol_ShutDown, searchapi/ISearchProtocol::ShutDown
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
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	ISearchProtocol.ShutDown
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ISearchProtocol::ShutDown method


## -description



            Shuts down the protocol handler.
        


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




            This method is called by the protocol host to enable the protocol handler to clean up and release any associated resources.
          


            The protocol host makes one call to this method before it exits. After this method is called, this instance will not be used any more. However, it is also possible for the protocol host process to terminate abruptly without calling this method. Protocol handlers that have persisted global states, such as registry entries and temporary files, should verify that those resources are cleaned up in the <a href="https://msdn.microsoft.com/f055f283-4b2f-4dcb-aed6-1e2ae24f2518">ISearchProtocol::Init</a> method before initialization.
          



