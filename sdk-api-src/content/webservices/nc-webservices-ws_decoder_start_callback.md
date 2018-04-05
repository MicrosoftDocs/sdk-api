---
UID: NC:webservices.WS_DECODER_START_CALLBACK
title: WS_DECODER_START_CALLBACK
author: windows-driver-content
description: Starts decoding a message.
old-location: wsw\ws_decoder_start_callback.htm
old-project: wsw
ms.assetid: e607b5a2-4d4a-4e23-854d-b5168556bb69
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WS_DECODER_START_CALLBACK, WS_DECODER_START_CALLBACK callback function [Web Services for Windows], webservices/WS_DECODER_START_CALLBACK, wsw.ws_decoder_start_callback
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
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	WebServices.h
api_name:
-	WS_DECODER_START_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_DECODER_START_CALLBACK callback


## -description


Starts decoding a message.


## -parameters




### -param *encoderContext [in]


                    The decoder instance returned by the <a href="https://msdn.microsoft.com/85311349-5c82-4545-8a2b-d8b9e629f04d">WS_CREATE_DECODER_CALLBACK</a>.
                


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">

Ran out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>
 




## -remarks




              The decoder can use the callback passed to <a href="https://msdn.microsoft.com/85311349-5c82-4545-8a2b-d8b9e629f04d">WS_CREATE_DECODER_CALLBACK</a> to
              read the encoded data of the message.
            



