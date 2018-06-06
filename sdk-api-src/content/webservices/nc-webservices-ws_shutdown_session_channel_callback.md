---
UID: NC:webservices.WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK
title: WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK
author: windows-sdk-content
description: Handles the WsShutdownSessionChannel call for a WS_CUSTOM_CHANNEL_BINDING.
old-location: wsw\ws_shutdown_session_channel_callback.htm
old-project: wsw
ms.assetid: 7dba0ae5-5610-4b8f-bbe5-b89244779e2d
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK, WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK callback, WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK callback function [Web Services for Windows], webservices/WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK, wsw.ws_shutdown_session_channel_callback
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
 - WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK callback function


## -description


Handles the <a href="https://msdn.microsoft.com/db12b0b7-698e-4c74-b547-6c95d0c5fdb7">WsShutdownSessionChannel</a> call
                for a <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CUSTOM_CHANNEL_BINDING</a>.
            


## -parameters




### -param *channelInstance [in]


                    The pointer to the state specific to this channel instance,
                    as created by the <a href="https://msdn.microsoft.com/440114f9-2258-4c33-93cd-7185ccf36f76">WS_CREATE_CHANNEL_CALLBACK</a>.
                


### -param *asyncContext [in, optional]


                    Information on how to invoke the function asynchronously, or <b>NULL</b> if invoking synchronously.
                


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

                    This is returned if the channel is not in the <a href="https://msdn.microsoft.com/3a7f5bbd-e484-4a7e-8e5d-df229a7227a5">WS_CHANNEL_STATE_OPEN</a> state.
                

</td>
</tr>
</table>
 




## -remarks




                See <a href="https://msdn.microsoft.com/db12b0b7-698e-4c74-b547-6c95d0c5fdb7">WsShutdownSessionChannel</a> for information about the contract
                of this API.
            



