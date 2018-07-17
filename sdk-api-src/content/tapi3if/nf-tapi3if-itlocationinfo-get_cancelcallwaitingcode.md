---
UID: NF:tapi3if.ITLocationInfo.get_CancelCallWaitingCode
title: ITLocationInfo::get_CancelCallWaitingCode
author: windows-sdk-content
description: The get_CancelCallWaitingCode method gets the dial digits and modifier characters that must be prefixed to a dialable string to cancel call waiting.
old-location: tapi3\itlocationinfo_get_cancelcallwaitingcode.htm
old-project: tapi
ms.assetid: 49137921-7354-4080-8684-148beb919f01
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITLocationInfo interface [TAPI 2.2],get_CancelCallWaitingCode method, ITLocationInfo.get_CancelCallWaitingCode, ITLocationInfo::get_CancelCallWaitingCode, _tapi3_itlocationinfo_get_cancelcallwaitingcode, get_CancelCallWaitingCode, get_CancelCallWaitingCode method [TAPI 2.2], get_CancelCallWaitingCode method [TAPI 2.2],ITLocationInfo interface, tapi3.itlocationinfo_get_cancelcallwaitingcode, tapi3if/ITLocationInfo::get_CancelCallWaitingCode
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITLocationInfo.get_CancelCallWaitingCode
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITLocationInfo::get_CancelCallWaitingCode


## -description


The 
<b>get_CancelCallWaitingCode</b> method gets the dial digits and modifier characters that must be prefixed to a dialable string to cancel call waiting.


## -parameters




### -param ppCode [out]

Pointer to <b>BSTR</b> representation of dial digits and modifier characters required to cancel call waiting.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppCode</i> parameter is not a valid pointer.

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



The application must use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory allocated for the <i>ppCode</i> parameter.
			

The value that this method returns corresponds to the <b>dwCancelCallWaitingSize</b> and <b>dwCancelCallWaitingOffset</b> members of TAPI 2's 
<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/0f82a6f4-26a6-48dc-9bfa-a86edf1b6be4">ITLocationInfo</a>



<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a>



<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a>
 

 

