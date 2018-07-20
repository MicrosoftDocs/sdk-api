---
UID: NF:webservices.WsEndReaderCanonicalization
title: WsEndReaderCanonicalization function
author: windows-sdk-content
description: This function stops XML canonicalization started by a preceding WsStartReaderCanonicalization function call. Any remaining canonical bytes buffered by the reader will be written to the callback function.
old-location: wsw\wsendreadercanonicalization.htm
old-project: wsw
ms.assetid: 5cacad47-8581-4713-96cb-3b3a863e6327
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WsEndReaderCanonicalization, WsEndReaderCanonicalization function [Web Services for Windows], webservices/WsEndReaderCanonicalization, wsw.wsendreadercanonicalization
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - WsEndReaderCanonicalization
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsEndReaderCanonicalization function


## -description



        This function stops XML canonicalization started by a preceding <a href="https://msdn.microsoft.com/5dad9485-db3c-4ae0-b053-e1e4f32ad64d">WsStartReaderCanonicalization</a> function call.
      
        Any remaining canonical bytes buffered by the reader will be written to the callback function.


## -parameters




### -param reader [in]

A pointer to the XML reader on which canonicalization should be stopped.


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


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
        which <a href="https://msdn.microsoft.com/5dad9485-db3c-4ae0-b053-e1e4f32ad64d">WsStartReaderCanonicalization</a> was called.
      


        It is not necessary to call <b>WsEndReaderCanonicalization</b>
        in order to call <a href="https://msdn.microsoft.com/31163bea-266f-43a3-bdf5-61386ebc197c">WsFreeReader</a>.
      



