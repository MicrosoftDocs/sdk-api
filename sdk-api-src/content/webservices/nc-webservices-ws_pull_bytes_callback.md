---
UID: NC:webservices.WS_PULL_BYTES_CALLBACK
title: WS_PULL_BYTES_CALLBACK
author: windows-sdk-content
description: Used by the WsPullBytes function to request the data that should be written.
old-location: wsw\ws_pull_bytes_callback.htm
old-project: wsw
ms.assetid: 84634ecc-056f-4fcc-838e-93f0dfc06e8d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WS_PULL_BYTES_CALLBACK, WS_PULL_BYTES_CALLBACK callback, WS_PULL_BYTES_CALLBACK callback function [Web Services for Windows], webservices/WS_PULL_BYTES_CALLBACK, wsw.ws_pull_bytes_callback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: webservices.h
req.include-header: 
req.redist: 
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
 - WS_PULL_BYTES_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_PULL_BYTES_CALLBACK callback function


## -description


Used by the <a href="https://msdn.microsoft.com/39e25db6-e51f-45cb-9739-260e7c246fcc">WsPullBytes</a> function to request 
        the data that should be written.
      


## -parameters




### -param *callbackState [in]

The user-defined state that was passed to <a href="https://msdn.microsoft.com/39e25db6-e51f-45cb-9739-260e7c246fcc">WsPullBytes</a>.
        


### -param *bytes

Where the data that is read should be placed.
        


### -param maxSize [in]

The maximum number of bytes that may be read.
        


### -param *actualSize [out]

The actual number of bytes that were read.  This may be less than maxSize.  Returning 0
          indicates that there is no more data.
        


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
<dt><b>WS_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation is still pending.
        

</td>
</tr>
</table>
 




## -remarks



Returning size of 0 indicates EOF.
      



