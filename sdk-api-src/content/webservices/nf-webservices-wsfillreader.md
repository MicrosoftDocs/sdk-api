---
UID: NF:webservices.WsFillReader
title: WsFillReader function
author: windows-sdk-content
description: Ensures that the reader has buffered the minimum byte count of XML data for use by subsequent reader functions.
old-location: wsw\wsfillreader.htm
old-project: wsw
ms.assetid: 1f4138a2-acc5-4f1d-8e35-544859d2fa49
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WsFillReader, WsFillReader function [Web Services for Windows], webservices/WsFillReader, wsw.wsfillreader
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
-	WsFillReader
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsFillReader function


## -description


Ensures that the reader has buffered the minimum byte count of XML data for use by subsequent reader functions.  It will invoke the callback specified by <a href="https://msdn.microsoft.com/53537eb2-6b8d-443e-9453-4b39dfef1dd7">WS_XML_READER_STREAM_INPUT</a>
        as many times as necessary to obtain the number of bytes specified by the value of the <i>minSize</i> parameter.  On completion the buffered data is available to other reader functions.  If a subsequent reader function requires more data than what has been obtained the function
        will return a <b>WS_E_QUOTA_EXCEEDED</b> exception.
      (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)


## -parameters




### -param reader [in]

A  pointer to a <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> structure used for obtaining the data.
                


### -param minSize [in]

Specifies the minimum number of bytes that the reader should have obtained.  If the current byte count buffered is equal to or greater than the value of <i>minSize</i> the function will do nothing and will return immediately.
        


### -param asyncContext [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/3c9ffbef-2f5b-42b0-96b1-f17f0ab98ca4">WS_ASYNC_CONTEXT</a> data structure with information about invoking the function asynchronously.  A <b>NULL</b> 
                 value indicates a request for synchronous operation.


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
<dt><b>WS_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">

          The asynchronous operation is still pending.
        

</td>
</tr>
</table>
 




## -remarks




        The number of bytes required to read a particular segment of XML data depends upon the encoding
        and its formatting.
      


        This function is a "no-op" when used with a reader using <a href="https://msdn.microsoft.com/86277c29-d42f-4b6a-ba33-b836bef284e7">WS_XML_READER_BUFFER_INPUT</a>.
      


        By specifying a <a href="https://msdn.microsoft.com/3c9ffbef-2f5b-42b0-96b1-f17f0ab98ca4">WS_ASYNC_CONTEXT</a> the data is read asynchronously.
      



