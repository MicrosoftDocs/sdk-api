---
UID: NF:tapi3if.ITCallingCard.get_InternationalDialingRule
title: ITCallingCard::get_InternationalDialingRule
author: windows-sdk-content
description: The get_InternationalDialingRule method gets the international dialing rules for this calling card.
old-location: tapi3\itcallingcard_get_internationaldialingrule.htm
tech.root: Tapi
ms.assetid: b452edbd-2c37-4f40-873b-24b4b60836bb
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITCallingCard interface [TAPI 2.2],get_InternationalDialingRule method, ITCallingCard.get_InternationalDialingRule, ITCallingCard::get_InternationalDialingRule, _tapi3_itcallingcard_get_internationaldialingrule, get_InternationalDialingRule, get_InternationalDialingRule method [TAPI 2.2], get_InternationalDialingRule method [TAPI 2.2],ITCallingCard interface, tapi3.itcallingcard_get_internationaldialingrule, tapi3if/ITCallingCard::get_InternationalDialingRule
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
 - ITCallingCard.get_InternationalDialingRule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallingCard::get_InternationalDialingRule


## -description


The 
<b>get_InternationalDialingRule</b> method gets the international dialing rules for this calling card.


## -parameters




### -param ppRule [out]

Pointer to <b>BSTR</b> representation of international dialing rules.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppRule</i> parameter is not a valid pointer.

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
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory allocated for the <i>ppRule</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/09787cd2-56b5-4ed2-8783-f3c53ce2cc66">ITCallingCard</a>
 

 

