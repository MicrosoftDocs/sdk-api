---
UID: NS:webservices._WS_SERVICE_CONTRACT
title: "_WS_SERVICE_CONTRACT"
author: windows-sdk-content
description: Specifies a service contract on an endpoint.
old-location: wsw\ws_service_contract.htm
tech.root: wsw
ms.assetid: 77bd8c1e-0596-44d7-be99-356d052ee6c1
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WS_SERVICE_CONTRACT, WS_SERVICE_CONTRACT structure [Web Services for Windows], _WS_SERVICE_CONTRACT, webservices/WS_SERVICE_CONTRACT, wsw.ws_service_contract
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SERVICE_CONTRACT
product: Windows
targetos: Windows
req.typenames: WS_SERVICE_CONTRACT
req.redist: 
---

# _WS_SERVICE_CONTRACT structure


## -description


Specifies a service contract on an <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">endpoint</a>.
            


## -struct-fields




### -field contractDescription

The typed contract metadata. See <a href="https://msdn.microsoft.com/0b2a5516-6faf-43d5-9370-a25dbc7e2843">WS_CONTRACT_DESCRIPTION</a>. Optional, if <b>defaultMessageHandlerCallback</b> is given.
                


### -field defaultMessageHandlerCallback

Callback for processing unhandled messages. Optional if contractDescription is given. 
                


### -field methodTable

The function table. Mandatory, if <b>contractDescription</b> is given.
                

