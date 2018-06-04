---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ISearchProtocol::ShutDown


## -description



            Shuts down the protocol handler.
        


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




            This method is called by the protocol host to enable the protocol handler to clean up and release any associated resources.
          


            The protocol host makes one call to this method before it exits. After this method is called, this instance will not be used any more. However, it is also possible for the protocol host process to terminate abruptly without calling this method. Protocol handlers that have persisted global states, such as registry entries and temporary files, should verify that those resources are cleaned up in the <a href="https://msdn.microsoft.com/f055f283-4b2f-4dcb-aed6-1e2ae24f2518">ISearchProtocol::Init</a> method before initialization.
          



