---
UID: NF:tapi3if.ITLocationInfo.get_TollPrefixList
title: ITLocationInfo::get_TollPrefixList
author: windows-sdk-content
description: The get_TollPrefixList method gets the toll prefix list.
old-location: tapi3\itlocationinfo_get_tollprefixlist.htm
old-project: Tapi
ms.assetid: 45297e46-b1c8-45b0-bb16-8c5d5666bbd0
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITLocationInfo interface [TAPI 2.2],get_TollPrefixList method, ITLocationInfo.get_TollPrefixList, ITLocationInfo::get_TollPrefixList, _tapi3_itlocationinfo_get_tollprefixlist, get_TollPrefixList, get_TollPrefixList method [TAPI 2.2], get_TollPrefixList method [TAPI 2.2],ITLocationInfo interface, tapi3.itlocationinfo_get_tollprefixlist, tapi3if/ITLocationInfo::get_TollPrefixList
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
 - ITLocationInfo.get_TollPrefixList
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITLocationInfo::get_TollPrefixList


## -description


The 
<b>get_TollPrefixList</b> method gets the toll prefix list.


## -parameters




### -param ppTollList [out]

Pointer to the <b>BSTR</b> containing a list of toll prefixes.


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
The <i>ppTollList</i> parameter is not a valid pointer.

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
<a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory allocated for the <i>ppTollList</i> parameter.
			

The value that this method returns corresponds to the <b>dwTollPrefixListSize</b> and <b>dwTollPrefixListOffset</b> members of TAPI 2's 
<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/0f82a6f4-26a6-48dc-9bfa-a86edf1b6be4">ITLocationInfo</a>



<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a>



<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a>
 

 

