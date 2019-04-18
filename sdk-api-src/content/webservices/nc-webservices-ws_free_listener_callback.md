---
UID: NC:webservices.WS_FREE_LISTENER_CALLBACK
title: WS_FREE_LISTENER_CALLBACK (webservices.h)
author: windows-sdk-content
description: Handles the WsFreeListener call for a WS_CUSTOM_CHANNEL_BINDING.
old-location: wsw\ws_free_listener_callback.htm
tech.root: wsw
ms.assetid: fd60ae42-5b3f-4482-b785-541f7379ab3e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_FREE_LISTENER_CALLBACK, WS_FREE_LISTENER_CALLBACK callback, WS_FREE_LISTENER_CALLBACK callback function [Web Services for Windows], webservices/WS_FREE_LISTENER_CALLBACK, wsw.ws_free_listener_callback
ms.topic: callback
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_FREE_LISTENER_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WS_FREE_LISTENER_CALLBACK callback function


## -description


Handles the <a href="https://msdn.microsoft.com/3a8a4cd3-d98e-467b-bbed-5cbd66f892ed">WsFreeListener</a> call
                for a <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CUSTOM_CHANNEL_BINDING</a>.
            


## -parameters




### -param *listenerInstance [in]

The pointer to the state specific to this listener instance,
                    as created by the <a href="https://msdn.microsoft.com/2d8e476d-dc68-44b4-b53b-be440a32efda">WS_CREATE_LISTENER_CALLBACK</a>.
                

The callback should free this pointer.
                


## -returns



This callback function does not return a value.




## -remarks



See <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a> for information about the contract
                of this API.
            



