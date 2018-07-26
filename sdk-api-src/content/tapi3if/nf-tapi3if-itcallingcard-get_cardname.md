---
UID: NF:tapi3if.ITCallingCard.get_CardName
title: ITCallingCard::get_CardName
author: windows-sdk-content
description: The get_CardName method gets the friendly name for the calling card.
old-location: tapi3\itcallingcard_get_cardname.htm
old-project: tapi
ms.assetid: d971d5ef-30d0-42a4-9a23-5b1388a0cb26
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITCallingCard interface [TAPI 2.2],get_CardName method, ITCallingCard.get_CardName, ITCallingCard::get_CardName, _tapi3_itcallingcard_get_cardname, get_CardName, get_CardName method [TAPI 2.2], get_CardName method [TAPI 2.2],ITCallingCard interface, tapi3.itcallingcard_get_cardname, tapi3if/ITCallingCard::get_CardName
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
 - ITCallingCard.get_CardName
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCallingCard::get_CardName


## -description


The 
<b>get_CardName</b> method gets the friendly name for the calling card.


## -parameters




### -param ppCardName [out]

Pointer to <b>BSTR</b> containing a displayable name for the calling card.


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
The <i>ppCardName</i> parameter is not a valid pointer.

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
<a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory allocated for the <i>ppCardName</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/09787cd2-56b5-4ed2-8783-f3c53ce2cc66">ITCallingCard</a>
 

 

