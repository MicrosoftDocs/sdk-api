---
UID: NF:tapi3if.ITAddressCapabilities.get_CompletionMessages
title: ITAddressCapabilities::get_CompletionMessages
author: windows-driver-content
description: The get_CompletionMessages gets completion messages. This method is provided for Automation client applications, such as those written in Visual Basic and scripting languages.
old-location: tapi3\itaddresscapabilities_get_completionmessages.htm
old-project: Tapi
ms.assetid: 0b2d9065-e519-4e76-b6a0-b62e19ecaf70
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: ITAddressCapabilities interface [TAPI 2.2],get_CompletionMessages method, ITAddressCapabilities.get_CompletionMessages, ITAddressCapabilities::get_CompletionMessages, _tapi3_itaddresscapabilities_get_completionmessages, get_CompletionMessages, get_CompletionMessages method [TAPI 2.2], get_CompletionMessages method [TAPI 2.2],ITAddressCapabilities interface, tapi3.itaddresscapabilities_get_completionmessages, tapi3if/ITAddressCapabilities::get_CompletionMessages
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITAddressCapabilities.get_CompletionMessages
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAddressCapabilities::get_CompletionMessages


## -description


The 
<b>get_CompletionMessages</b> gets completion messages. This method is provided for Automation client applications, such as those written in Visual Basic and scripting languages.


## -parameters




### -param pVariant [out]

Pointer to <b>VARIANT</b> containing completion messages.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/36f452ce-9171-41da-b003-4c7df17790da">ITAddressCapabilities</a>
 

 

