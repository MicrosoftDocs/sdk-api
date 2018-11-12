---
UID: NF:tapi3if.ITCallingCard.get_SameAreaDialingRule
title: ITCallingCard::get_SameAreaDialingRule
author: windows-sdk-content
description: The get_SameAreaDialingRule method gets the dialing rules for calls within the same area code.
old-location: tapi3\itcallingcard_get_sameareadialingrule.htm
tech.root: tapi
ms.assetid: d8539040-a988-4d96-8cf1-9ec8ff46a0a9
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITCallingCard interface [TAPI 2.2],get_SameAreaDialingRule method, ITCallingCard.get_SameAreaDialingRule, ITCallingCard::get_SameAreaDialingRule, _tapi3_itcallingcard_get_sameareadialingrule, get_SameAreaDialingRule, get_SameAreaDialingRule method [TAPI 2.2], get_SameAreaDialingRule method [TAPI 2.2],ITCallingCard interface, tapi3.itcallingcard_get_sameareadialingrule, tapi3if/ITCallingCard::get_SameAreaDialingRule
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
 - ITCallingCard.get_SameAreaDialingRule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallingCard::get_SameAreaDialingRule


## -description


The 
<b>get_SameAreaDialingRule</b> method gets the dialing rules for calls within the same area code.


## -parameters




### -param ppRule [out]

Pointer to <b>BSTR</b> representation of local area dialing rules.


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
The <i>ppRule</i> parameter is not a valid pointer.

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
<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory allocated for the <i>ppRule</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/09787cd2-56b5-4ed2-8783-f3c53ce2cc66">ITCallingCard</a>
 

 

