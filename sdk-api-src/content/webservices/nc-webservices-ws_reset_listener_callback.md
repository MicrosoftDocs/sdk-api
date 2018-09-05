---
UID: NC:webservices.WS_RESET_LISTENER_CALLBACK
title: WS_RESET_LISTENER_CALLBACK
author: windows-sdk-content
description: Handles the WsResetListener call for a WS_CUSTOM_CHANNEL_BINDING.
old-location: wsw\ws_reset_listener_callback.htm
old-project: wsw
ms.assetid: 98a48403-5ac6-44c2-8a43-c81746390a0d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WS_RESET_LISTENER_CALLBACK, WS_RESET_LISTENER_CALLBACK callback, WS_RESET_LISTENER_CALLBACK callback function [Web Services for Windows], webservices/WS_RESET_LISTENER_CALLBACK, wsw.ws_reset_listener_callback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: webservices.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_RESET_LISTENER_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_RESET_LISTENER_CALLBACK callback function


## -description


Handles the <a href="https://msdn.microsoft.com/c23c8ad4-a193-42f2-9e4a-3e814b7bbdb2">WsResetListener</a> call
                for a <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CUSTOM_CHANNEL_BINDING</a>.
            


## -parameters




### -param *listenerInstance [in]

The pointer to the state specific to this listener instance,
                    as created by the <a href="https://msdn.microsoft.com/2d8e476d-dc68-44b4-b53b-be440a32efda">WS_CREATE_LISTENER_CALLBACK</a>.
                


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
The listener was in an inappropriate state.
                

</td>
</tr>
</table>
 




## -remarks



See <a href="https://msdn.microsoft.com/c23c8ad4-a193-42f2-9e4a-3e814b7bbdb2">WsResetListener</a> for information about the contract
                of this API.
            



