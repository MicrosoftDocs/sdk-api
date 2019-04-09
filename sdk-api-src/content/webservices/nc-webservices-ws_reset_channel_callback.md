---
UID: NC:webservices.WS_RESET_CHANNEL_CALLBACK
title: WS_RESET_CHANNEL_CALLBACK (webservices.h)
author: windows-sdk-content
description: Handles the WsResetChannel call for a WS_CUSTOM_CHANNEL_BINDING.
old-location: wsw\ws_reset_channel_callback.htm
tech.root: wsw
ms.assetid: 3f3b4995-72ca-4e93-87de-89996f9c43cb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_RESET_CHANNEL_CALLBACK, WS_RESET_CHANNEL_CALLBACK callback, WS_RESET_CHANNEL_CALLBACK callback function [Web Services for Windows], webservices/WS_RESET_CHANNEL_CALLBACK, wsw.ws_reset_channel_callback
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
 - WS_RESET_CHANNEL_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WS_RESET_CHANNEL_CALLBACK callback function


## -description


Handles the <a href="https://msdn.microsoft.com/7aca8ae0-44a0-4ec7-87e8-bec9bd17d04b">WsResetChannel</a> call
                for a <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CUSTOM_CHANNEL_BINDING</a>.
            


## -parameters




### -param *channelInstance [in]

The pointer to the state specific to this channel instance,
                    as created by the <a href="https://msdn.microsoft.com/440114f9-2258-4c33-93cd-7185ccf36f76">WS_CREATE_CHANNEL_CALLBACK</a>.
                


### -param *error [in, optional]

Specifies where additional error information should be stored if the function fails.
                


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The channel was in an inappropriate state.
                

</td>
</tr>
</table>
 




## -remarks



See <a href="https://msdn.microsoft.com/7aca8ae0-44a0-4ec7-87e8-bec9bd17d04b">WsResetChannel</a> for information about the contract
                of this API.
            



