---
UID: NF:tapi3if.ITLocationInfo.get_LocationName
title: ITLocationInfo::get_LocationName
author: windows-sdk-content
description: The get_LocationName method gets the location name.
old-location: tapi3\itlocationinfo_get_locationname.htm
old-project: tapi
ms.assetid: 2bd86295-8240-477d-90aa-f3061666c5e6
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITLocationInfo interface [TAPI 2.2],get_LocationName method, ITLocationInfo.get_LocationName, ITLocationInfo::get_LocationName, _tapi3_itlocationinfo_get_locationname, get_LocationName, get_LocationName method [TAPI 2.2], get_LocationName method [TAPI 2.2],ITLocationInfo interface, tapi3.itlocationinfo_get_locationname, tapi3if/ITLocationInfo::get_LocationName
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
 - ITLocationInfo.get_LocationName
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITLocationInfo::get_LocationName


## -description


The 
<b>get_LocationName</b> method gets the location name.


## -parameters




### -param ppLocationName [out]

Pointer to the <b>BSTR</b> representation of the location name.


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
The <i>ppLocationName</i> parameter is not a valid pointer.

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
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory allocated for the <i>ppLocationName</i> parameter.
			

The value that this method returns corresponds to the <b>dwLocationNameSize</b> and <b>dwLocationNameOffset</b> members of TAPI 2's 
<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/0f82a6f4-26a6-48dc-9bfa-a86edf1b6be4">ITLocationInfo</a>



<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a>



<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a>
 

 

