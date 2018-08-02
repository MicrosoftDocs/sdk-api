---
UID: NC:webservices.WS_CREATE_DECODER_CALLBACK
title: WS_CREATE_DECODER_CALLBACK
author: windows-sdk-content
description: Handles creating an decoder instance.
old-location: wsw\ws_create_decoder_callback.htm
old-project: wsw
ms.assetid: 85311349-5c82-4545-8a2b-d8b9e629f04d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WS_CREATE_DECODER_CALLBACK, WS_CREATE_DECODER_CALLBACK callback, WS_CREATE_DECODER_CALLBACK callback function [Web Services for Windows], webservices/WS_CREATE_DECODER_CALLBACK, wsw.ws_create_decoder_callback
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
 - WS_CREATE_DECODER_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_CREATE_DECODER_CALLBACK callback function


## -description


Handles creating an decoder instance.
            


## -parameters




### -param *createContext [in]

The createContext that was specified in the <a href="https://msdn.microsoft.com/d634f203-cf98-4f4e-85ce-5df23653a3ad">WS_CHANNEL_DECODER</a>used during channel creation.
                


### -param readCallback [in]

The function that should be used to read the message data.  This callback
                    should only be used in response to the <a href="https://msdn.microsoft.com/e607b5a2-4d4a-4e23-854d-b5168556bb69">WS_DECODER_START_CALLBACK</a>,
                    <a href="https://msdn.microsoft.com/04ba9b13-8145-4956-85b2-2330c792665a">WS_DECODER_DECODE_CALLBACK</a> and <a href="https://msdn.microsoft.com/7cf93467-84f6-4ffb-8329-bc1df119087a">WS_DECODER_END_CALLBACK</a> 
                    callbacks.
                


### -param *readContext [in]

The read context that should be passed to the provided <a href="https://msdn.microsoft.com/2a5ebe4a-e97d-4744-9ec9-da6da892e4c5">WS_READ_CALLBACK</a>.
                


#### - **decoderContext

Returns the decoder instance.  This value will be
                    passed to all of the decoder callbacks.
                


### -param *error [in, optional]

Specifies where additional error information should be stored if the function fails.
                


#### - decoderContext

Returns the decoder instance.  This value will be
                    passed to all of the decoder callbacks.
                


## -returns



This callback function can return one of these values.

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



The channel will create decoder instances as necessary.  Each decoder
               instance will be called in a single-threaded fashion.  A single decoder 
               instance however should not assume that it will see all messages from a
               channel, as the channel may use multiple decoder instances for processing
               messages.
            



