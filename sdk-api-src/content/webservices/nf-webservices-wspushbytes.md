---
UID: NF:webservices.WsPushBytes
title: WsPushBytes function
author: windows-sdk-content
description: Establishes a callback to be invoked to write bytes within an element. In some encodings this can be more efficient by eliminating a copy of the data.
old-location: wsw\wspushbytes.htm
old-project: wsw
ms.assetid: 295eb530-00f1-4e80-bd8a-ffb3eb1fad5b
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WsPushBytes, WsPushBytes function [Web Services for Windows], webservices/WsPushBytes, wsw.wspushbytes
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WebServices.dll
api_name:
-	WsPushBytes
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsPushBytes function


## -description


Establishes a callback to be invoked to write bytes within an element.  In some encodings this can
        be more efficient by eliminating a copy of the data.
      


## -parameters




### -param writer [in]

A pointer to the XML Writer object to which the bytes are written.  The pointer must reference a valid <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> and   the referenced value may not be <b>NULL</b>.
                


### -param callback [in]

This parameter is the callback to invoke to write the data.
        


### -param callbackState [in, optional]

A pointer to a user-defined state that is  passed to the callback function.
        


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




        When writing with the <a href="https://msdn.microsoft.com/18236818-492f-4906-9e7d-6ca03ef28d36">WS_XML_WRITER_MTOM_ENCODING</a>, <b>WsPushBytes</b> provides a way
        to write bytes directly into its own MIME part and avoid a copy.  However, the writer at its discretion,
        may choose to invoke the callback immediately, so the caller should be prepared for this.
      


        If the encoding cannot take advantage of this behavior, then <b>WsPushBytes</b> will invoke the
        callback immediately and operate as if <a href="https://msdn.microsoft.com/1fa9ecfc-c791-459f-ae11-ffcdc82b7145">WsWriteBytes</a> was called.
      



