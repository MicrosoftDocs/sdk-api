---
UID: NF:webservices.WsResetChannel
title: WsResetChannel function
author: windows-driver-content
description: Reset a channel so it can be reused.
old-location: wsw\wsresetchannel.htm
old-project: wsw
ms.assetid: 7aca8ae0-44a0-4ec7-87e8-bec9bd17d04b
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WsResetChannel, WsResetChannel function [Web Services for Windows], webservices/WsResetChannel, wsw.wsresetchannel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WebServices.dll
api_name:
-	WsResetChannel
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsResetChannel function


## -description



                Reset a channel so it can be reused.
            


## -parameters




### -param channel [in]


                    The channel to reset.
                


### -param error [in, optional]


                    Specifies where additional error information should be stored if the function fails.
                


## -returns



This function can return one of these values.

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




                Reusing a channel instead of creating one from scratch may improve performance.
            


                This function is only valid when the channel is in the either the
                <a href="https://msdn.microsoft.com/3a7f5bbd-e484-4a7e-8e5d-df229a7227a5">WS_CHANNEL_STATE_CREATED</a> or <b>WS_CHANNEL_STATE_CLOSED</b> state.
            


                If called correctly, this function will not fail (for example, due to lack of system resources).
            



