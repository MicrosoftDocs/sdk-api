---
UID: NF:webservices.WsReadCharsUtf8
title: WsReadCharsUtf8 function
author: windows-sdk-content
description: Reads a specified number of text characters from the reader and returns them encoded in UTF-8.
old-location: wsw\wsreadcharsutf8.htm
old-project: wsw
ms.assetid: 03326291-a61b-457b-80ca-dbe5bef6bf9d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WsReadCharsUtf8, WsReadCharsUtf8 function [Web Services for Windows], webservices/WsReadCharsUtf8, wsw.wsreadcharsutf8
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
 - WsReadCharsUtf8
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsReadCharsUtf8 function


## -description


Reads a specified number of text characters from the reader and returns them encoded in UTF-8.
      


## -parameters




### -param reader [in]

A pointer to the <b>XML Reader</b> from which the character data should be read.  The pointer must reference a valid <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> object.
        


### -param bytes

A pointer to the buffer to place the encoded bytes that have been read.


### -param maxByteCount [in]

The maximum number of bytes that should be read.


### -param actualByteCount [out]

A pointer to a ULONG value of 
          the actual number of bytes that were read.  This may be less than maxByteCount even when there
          are more bytes remaining.  There are no more bytes when this returns zero.
        


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
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

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



XML text is read up to either a start element or end element.  Comments are skipped, and CDATA content is treated
        identically to element content.    Character entities are converted to their unescaped form.
      

This function can fail for any of the reasons listed in <a href="https://msdn.microsoft.com/60dacf3e-ebde-4247-be58-835565874ab6">WsReadNode</a>.
      



