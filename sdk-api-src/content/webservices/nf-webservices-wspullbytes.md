---
UID: NF:webservices.WsPullBytes
title: WsPullBytes function
author: windows-sdk-content
description: Sets up a callback to be invoked to obtain the bytes to be written within an element. In some encodings this can be more efficient by eliminating a copy of the data.
old-location: wsw\wspullbytes.htm
old-project: wsw
ms.assetid: 39e25db6-e51f-45cb-9739-260e7c246fcc
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WsPullBytes, WsPullBytes function [Web Services for Windows], webservices/WsPullBytes, wsw.wspullbytes
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsPullBytes
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsPullBytes function


## -description



        Sets up a callback to be invoked to obtain the bytes to be written within an element.  
        In some encodings this can be more efficient by eliminating a copy of the data.
      


## -parameters




### -param writer [in]


          The writer to which the bytes will be written.
        


### -param callback [in]


          The callback to invoke when its time to write the binary data.
        


### -param callbackState [in, optional]


          User-defined state to be passed to the callback.
        


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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">

The operation is not allowed due to the current state of the object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">

A quota was exceeded.

</td>
</tr>
</table>
 




## -remarks




<a href="https://msdn.microsoft.com/1fa9ecfc-c791-459f-ae11-ffcdc82b7145">WsWriteBytes</a> and <a href="https://msdn.microsoft.com/295eb530-00f1-4e80-bd8a-ffb3eb1fad5b">WsPushBytes</a> require the buffer of data to be provided to the writer.
        In some usage patterns, this may require an extra copy of the data.  For those scenarios, <b>WsPullBytes</b>
        offers a way to request the writer to provide the buffer that must be filled with data.
      


        If the encoding cannot take advantage of this behavior, then <b>WsPullBytes</b> will invoke the
        callback immediately and operate as if <a href="https://msdn.microsoft.com/1fa9ecfc-c791-459f-ae11-ffcdc82b7145">WsWriteBytes</a> was called on the resulting data.
      



