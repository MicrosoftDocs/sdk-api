---
UID: NC:webservices.WS_ABORT_CHANNEL_CALLBACK
title: WS_ABORT_CHANNEL_CALLBACK
author: windows-sdk-content
description: Handles the WsAbortChannel call for a WS_CUSTOM_CHANNEL_BINDING.
old-location: wsw\ws_abort_channel_callback.htm
tech.root: wsw
ms.assetid: b2841065-5724-4fbb-92f0-b3b7ad1a6e26
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WS_ABORT_CHANNEL_CALLBACK, WS_ABORT_CHANNEL_CALLBACK callback, WS_ABORT_CHANNEL_CALLBACK callback function [Web Services for Windows], webservices/WS_ABORT_CHANNEL_CALLBACK, wsw.ws_abort_channel_callback
ms.prod: windows
ms.technology: windows-sdk
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
 - WS_ABORT_CHANNEL_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WS_ABORT_CHANNEL_CALLBACK callback function


## -description


Handles the <a href="https://msdn.microsoft.com/67af85d7-db75-4e26-a7cc-8115ac3f2d59">WsAbortChannel</a> call
                for a <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CUSTOM_CHANNEL_BINDING</a>.
            


## -parameters




### -param *channelInstance [in]

The pointer to the state specific to this channel instance,
                    as created by the <a href="https://msdn.microsoft.com/440114f9-2258-4c33-93cd-7185ccf36f76">WS_CREATE_CHANNEL_CALLBACK</a>.
                


### -param *error [in, optional]

Specifies where additional error information should be stored if the function fails.
                


## -returns



This callback function does not return a value.




## -remarks



See <a href="https://msdn.microsoft.com/67af85d7-db75-4e26-a7cc-8115ac3f2d59">WsAbortChannel</a> for information about the contract
                of this API.
            



