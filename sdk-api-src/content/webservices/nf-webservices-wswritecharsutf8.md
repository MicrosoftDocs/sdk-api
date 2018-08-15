---
UID: NF:webservices.WsWriteCharsUtf8
title: WsWriteCharsUtf8 function
author: windows-sdk-content
description: Writes a series of characters encoded as UTF-8 to an element or attribute.
old-location: wsw\wswritecharsutf8.htm
old-project: wsw
ms.assetid: 53cdaf22-21ed-4e5a-8034-d5a4725b9da3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WsWriteCharsUtf8, WsWriteCharsUtf8 function [Web Services for Windows], webservices/WsWriteCharsUtf8, wsw.wswritecharsutf8
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsWriteCharsUtf8
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsWriteCharsUtf8 function


## -description


Writes a series of characters encoded as UTF-8 to an element or attribute.
      To write characters to an attribute value, call <a href="https://msdn.microsoft.com/9fd1eed9-6d8b-4b2e-a7ad-54a7f584734f">WsWriteStartAttribute</a> first.
      Only whitespace characters may be written at the root of an xml document unless the
        <b>WS_XML_WRITER_PROPERTY_ALLOW_FRAGMENT</b> has been set to <b>TRUE</b>.
      


## -parameters




### -param writer [in]

A pointer to the <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> object to which the characters are written.  The pointer must reference a valid <b>XML Writer</b> object.
                


### -param bytes

A pointer to the encoded UTF-8 characters to write.
        


### -param byteCount [in]

The number of bytes to write.
        


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



<b>WsWriteCharsUtf8</b> can be called more than once between <a href="https://msdn.microsoft.com/9fd1eed9-6d8b-4b2e-a7ad-54a7f584734f">WsWriteStartAttribute</a> and <a href="https://msdn.microsoft.com/8747c484-19b3-46b2-beee-80b220011def">WsWriteEndAttribute</a>.  It cannot be combined with <a href="https://msdn.microsoft.com/e435058f-62b5-4ae9-800e-e022033a9664">WsWriteChars</a>, <a href="https://msdn.microsoft.com/1fa9ecfc-c791-459f-ae11-ffcdc82b7145">WsWriteBytes</a>, <a href="https://msdn.microsoft.com/c7b9d014-89b5-4959-b49e-ee2cdeb41f7c">WsWriteValue</a> or <a href="https://msdn.microsoft.com/a4ffc05e-d04a-4cc3-bdb6-71b2090bc32f">WsWriteText</a>when writing an attribute.
      



