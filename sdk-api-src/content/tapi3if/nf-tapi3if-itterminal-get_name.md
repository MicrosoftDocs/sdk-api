---
UID: NF:tapi3if.ITTerminal.get_Name
title: ITTerminal::get_Name
author: windows-sdk-content
description: The get_Name method gets a descriptive name of the terminal. The name must be usable to the user.
old-location: tapi3\itterminal_get_name.htm
old-project: Tapi
ms.assetid: ad3a44ff-ad63-4fd0-9cfd-c97c0cea6162
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITTerminal interface [TAPI 2.2],get_Name method, ITTerminal.get_Name, ITTerminal::get_Name, _tapi3_itterminal_get_name, get_Name, get_Name method [TAPI 2.2], get_Name method [TAPI 2.2],ITTerminal interface, tapi3.itterminal_get_name, tapi3if/ITTerminal::get_Name
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tapi3if.h
api_name:
-	ITTerminal.get_Name
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTerminal::get_Name


## -description


The 
<b>get_Name</b> method gets a descriptive name of the terminal. The name must be usable to the user.


## -parameters




### -param ppName [out]

Pointer to <b>BSTR</b> containing the name of the terminal.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppName</i> parameter is not a valid pointer.

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
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory allocated for the <i>ppName</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>



<a href="https://msdn.microsoft.com/08320d1c-1400-4746-b526-74b0789c5fc0">Terminal Object Interfaces</a>
 

 

