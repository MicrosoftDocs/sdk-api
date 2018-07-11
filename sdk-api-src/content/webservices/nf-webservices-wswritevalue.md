---
UID: NF:webservices.WsWriteValue
title: WsWriteValue function
author: windows-sdk-content
description: This operation derives the best representation for a primitive value from the underlying encoding and passes the derived value to a Writer object.
old-location: wsw\wswritevalue.htm
old-project: wsw
ms.assetid: c7b9d014-89b5-4959-b49e-ee2cdeb41f7c
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WsWriteValue, WsWriteValue function [Web Services for Windows], webservices/WsWriteValue, wsw.wswritevalue
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
 - WsWriteValue
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsWriteValue function


## -description



        This operation derives the best representation for a  primitive value from the underlying encoding and passes the derived value to a Writer object.
      <div class="alert"><b>Note</b>  It is generally more efficient to use this function to write out primitive values rather than converting
        the value to text and subsequently using <a href="https://msdn.microsoft.com/e435058f-62b5-4ae9-800e-e022033a9664">WsWriteChars</a>.</div>
<div> </div>



## -parameters




### -param writer [in]

A pointer to the <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> object to which the value is written.  The pointer must reference a valid <b>XML Writer</b> object.
                


### -param valueType [in]

Indicates the Type of primitive value referenced by the <i>value</i> parameter.


          I


### -param value

A void  pointer to the primitive value.  
                


### -param valueSize [in]

The size in bytes of the value being written.


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



<b>WsWriteValue</b> may be called only once between <a href="https://msdn.microsoft.com/9fd1eed9-6d8b-4b2e-a7ad-54a7f584734f">WsWriteStartAttribute</a> and <a href="https://msdn.microsoft.com/8747c484-19b3-46b2-beee-80b220011def">WsWriteEndAttribute</a>.
        It may not be combined with <a href="https://msdn.microsoft.com/e435058f-62b5-4ae9-800e-e022033a9664">WsWriteChars</a>, <a href="https://msdn.microsoft.com/1fa9ecfc-c791-459f-ae11-ffcdc82b7145">WsWriteBytes</a>, <a href="https://msdn.microsoft.com/53cdaf22-21ed-4e5a-8034-d5a4725b9da3">WsWriteCharsUtf8</a> or <a href="https://msdn.microsoft.com/a4ffc05e-d04a-4cc3-bdb6-71b2090bc32f">WsWriteText</a>
        when writing an attribute.
      



