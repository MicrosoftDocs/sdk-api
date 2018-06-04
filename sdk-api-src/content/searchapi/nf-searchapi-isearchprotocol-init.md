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
      



