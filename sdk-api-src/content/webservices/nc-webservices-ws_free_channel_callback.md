---
UID: NC:webservices.WS_FREE_CHANNEL_CALLBACK
title: WS_FREE_CHANNEL_CALLBACK
author: windows-sdk-content
description: Handles the WsFreeChannel call for a WS_CUSTOM_CHANNEL_BINDING.
old-location: wsw\ws_free_channel_callback.htm
tech.root: wsw
ms.assetid: f1781c50-824e-4b79-91b6-97e31581617a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_FREE_CHANNEL_CALLBACK, WS_FREE_CHANNEL_CALLBACK callback, WS_FREE_CHANNEL_CALLBACK callback function [Web Services for Windows], webservices/WS_FREE_CHANNEL_CALLBACK, wsw.ws_free_channel_callback
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WS_FREE_CHANNEL_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WS_FREE_CHANNEL_CALLBACK callback function


## -description


Handles the <a href="https://msdn.microsoft.com/74e36d19-c6db-4bba-90e3-88a48b6a1fb5">WsFreeChannel</a> call
                for a <a href="https://msdn.microsoft.com/en-us/library/Dd401780(v=VS.85).aspx">WS_CUSTOM_CHANNEL_BINDING</a>.
            


## -parameters




### -param *channelInstance [in]

The pointer to the state specific to this channel instance,
                    as created by the <a href="https://msdn.microsoft.com/440114f9-2258-4c33-93cd-7185ccf36f76">WS_CREATE_CHANNEL_CALLBACK</a>.
                

The callback should free this pointer.
                


## -returns



This callback function does not return a value.




## -remarks



See <a href="https://msdn.microsoft.com/a7226194-0974-4f3c-b92d-78a93e86eea5">WsOpenChannel</a> for information about the contract
                of this API.
            



