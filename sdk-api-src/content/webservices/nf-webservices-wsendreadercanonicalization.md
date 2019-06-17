---
UID: NF:webservices.WsEndReaderCanonicalization
title: WsEndReaderCanonicalization function (webservices.h)
author: windows-sdk-content
description: This function stops XML canonicalization started by a preceding WsStartReaderCanonicalization function call. Any remaining canonical bytes buffered by the reader will be written to the callback function.
old-location: wsw\wsendreadercanonicalization.htm
tech.root: wsw
ms.assetid: 5cacad47-8581-4713-96cb-3b3a863e6327
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WsEndReaderCanonicalization, WsEndReaderCanonicalization function [Web Services for Windows], webservices/WsEndReaderCanonicalization, wsw.wsendreadercanonicalization
ms.topic: function
f1_keywords: ["webservices/WsEndReaderCanonicalization"]
req.header: webservices.h
req.include-header: 
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
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsEndReaderCanonicalization
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WsEndReaderCanonicalization function


## -description


This function stops XML canonicalization started by a preceding <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsstartreadercanonicalization">WsStartReaderCanonicalization</a> function call.
      
        Any remaining canonical bytes buffered by the reader will be written to the callback function.


## -parameters




### -param reader [in]

A pointer to the XML reader on which canonicalization should be stopped.


### -param error [in, optional]

A  pointer to a <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


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
</table>
 




## -remarks



<b>WsEndReaderCanonicalization</b> must be called at the same depth at
        which <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsstartreadercanonicalization">WsStartReaderCanonicalization</a> was called.
      

It is not necessary to call <b>WsEndReaderCanonicalization</b>in order to call <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsfreereader">WsFreeReader</a>.
      



