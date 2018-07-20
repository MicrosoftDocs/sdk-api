---
UID: NF:tapi3if.ITLocationInfo.get_PermanentLocationID
title: ITLocationInfo::get_PermanentLocationID
author: windows-sdk-content
description: The get_PermanentLocationID method gets the permanent location identifier.
old-location: tapi3\itlocationinfo_get_permanentlocationid.htm
old-project: tapi
ms.assetid: 5dab6a20-6113-46ef-a5d2-855ac1befc1a
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITLocationInfo interface [TAPI 2.2],get_PermanentLocationID method, ITLocationInfo.get_PermanentLocationID, ITLocationInfo::get_PermanentLocationID, _tapi3_itlocationinfo_get_permanentlocationid, get_PermanentLocationID, get_PermanentLocationID method [TAPI 2.2], get_PermanentLocationID method [TAPI 2.2],ITLocationInfo interface, tapi3.itlocationinfo_get_permanentlocationid, tapi3if/ITLocationInfo::get_PermanentLocationID
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
 - ITLocationInfo.get_PermanentLocationID
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITLocationInfo::get_PermanentLocationID


## -description


The 
<b>get_PermanentLocationID</b> method gets the permanent location identifier.


## -parameters




### -param plLocationID [out]

Pointer to the permanent location identifier.


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
The <i>plLocationID</i> parameter is not a valid pointer.

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



The value that this method returns corresponds to the <b>dwPermanentLocationID</b> member of TAPI 2's 
<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/0f82a6f4-26a6-48dc-9bfa-a86edf1b6be4">ITLocationInfo</a>



<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a>



<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a>
 

 

