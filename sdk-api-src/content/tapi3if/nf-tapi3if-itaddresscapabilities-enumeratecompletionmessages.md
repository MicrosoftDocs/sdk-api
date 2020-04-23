---
UID: NF:tapi3if.ITAddressCapabilities.EnumerateCompletionMessages
title: ITAddressCapabilities::EnumerateCompletionMessages (tapi3if.h)
description: The EnumerateCompletionMessages method gets completion messages. This method is provided for applications written in C/C++ and Java.helpviewer_keywords: ["EnumerateCompletionMessages","EnumerateCompletionMessages method [TAPI 2.2]","EnumerateCompletionMessages method [TAPI 2.2]","ITAddressCapabilities interface","ITAddressCapabilities interface [TAPI 2.2]","EnumerateCompletionMessages method","ITAddressCapabilities.EnumerateCompletionMessages","ITAddressCapabilities::EnumerateCompletionMessages","_tapi3_itaddresscapabilities_enumeratecompletionmessages","tapi3.itaddresscapabilities_enumeratecompletionmessages","tapi3if/ITAddressCapabilities::EnumerateCompletionMessages"]
old-location: tapi3\itaddresscapabilities_enumeratecompletionmessages.htm
tech.root: Tapi
ms.assetid: b7a3eb72-6c9f-4164-a082-8b0951733dcb
ms.date: 12/05/2018
ms.keywords: EnumerateCompletionMessages, EnumerateCompletionMessages method [TAPI 2.2], EnumerateCompletionMessages method [TAPI 2.2],ITAddressCapabilities interface, ITAddressCapabilities interface [TAPI 2.2],EnumerateCompletionMessages method, ITAddressCapabilities.EnumerateCompletionMessages, ITAddressCapabilities::EnumerateCompletionMessages, _tapi3_itaddresscapabilities_enumeratecompletionmessages, tapi3.itaddresscapabilities_enumeratecompletionmessages, tapi3if/ITAddressCapabilities::EnumerateCompletionMessages
f1_keywords:
- tapi3if/ITAddressCapabilities.EnumerateCompletionMessages
dev_langs:
- c++
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITAddressCapabilities.EnumerateCompletionMessages
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAddressCapabilities::EnumerateCompletionMessages


## -description


The 
<b>EnumerateCompletionMessages</b> method gets completion messages. This method is provided for applications written in C/C++ and Java.


## -parameters




### -param ppEnumCompletionMessage [out]

Pointer to enumeration of completion messages.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr">IEnumBstr</a> interface returned by <b>ITAddressCapabilities::EnumerateCompletionMessages</b>. The application must call <b>Release</b> on the 
<b>IEnumBstr</b> interface to free resources associated with it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-object">Address Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr">IEnumBstr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities">ITAddressCapabilities</a>
 

 

