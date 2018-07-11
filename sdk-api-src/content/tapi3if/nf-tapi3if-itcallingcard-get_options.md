---
UID: NF:tapi3if.ITCallingCard.get_Options
title: ITCallingCard::get_Options
author: windows-sdk-content
description: The get_Options method gets the translation options for this address and card.
old-location: tapi3\itcallingcard_get_options.htm
old-project: tapi
ms.assetid: 0daa0058-759b-4f4c-8fb4-ce65e4fa9682
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITCallingCard interface [TAPI 2.2],get_Options method, ITCallingCard.get_Options, ITCallingCard::get_Options, _tapi3_itcallingcard_get_options, get_Options, get_Options method [TAPI 2.2], get_Options method [TAPI 2.2],ITCallingCard interface, tapi3.itcallingcard_get_options, tapi3if/ITCallingCard::get_Options
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
 - ITCallingCard.get_Options
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCallingCard::get_Options


## -description


The 
<b>get_Options</b> method gets the translation options for this address and card.


## -parameters




### -param plOptions [out]

Pointer to 
<a href="https://msdn.microsoft.com/3f5e9952-945e-42b8-8536-b52a0c833282">LINETRANSLATEOPTION</a> flags.


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
The <i>plOptions</i> parameter is not a valid pointer.

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




<a href="https://msdn.microsoft.com/09787cd2-56b5-4ed2-8783-f3c53ce2cc66">ITCallingCard</a>
 

 

