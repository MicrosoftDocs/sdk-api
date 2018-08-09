---
UID: NF:tapi3if.ITCallingCard.get_LongDistanceDialingRule
title: ITCallingCard::get_LongDistanceDialingRule
author: windows-sdk-content
description: The get_LongDistanceDialingRule method gets the long distance dialing rules for this calling card.
old-location: tapi3\itcallingcard_get_longdistancedialingrule.htm
old-project: tapi
ms.assetid: 97ad3528-ee84-4b61-9d08-55d3500432dd
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITCallingCard interface [TAPI 2.2],get_LongDistanceDialingRule method, ITCallingCard.get_LongDistanceDialingRule, ITCallingCard::get_LongDistanceDialingRule, _tapi3_itcallingcard_get_longdistancedialingrule, get_LongDistanceDialingRule, get_LongDistanceDialingRule method [TAPI 2.2], get_LongDistanceDialingRule method [TAPI 2.2],ITCallingCard interface, tapi3.itcallingcard_get_longdistancedialingrule, tapi3if/ITCallingCard::get_LongDistanceDialingRule
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
 - ITCallingCard.get_LongDistanceDialingRule
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCallingCard::get_LongDistanceDialingRule


## -description


The 
<b>get_LongDistanceDialingRule</b> method gets the long distance dialing rules for this calling card.


## -parameters




### -param ppRule [out]

Pointer to <b>BSTR</b> representation of long distance dialing rules.


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
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory allocated for the <i>ppRule</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/09787cd2-56b5-4ed2-8783-f3c53ce2cc66">ITCallingCard</a>
 

 

