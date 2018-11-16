---
UID: NF:mergemod.IMsmError.get_ModuleTable
title: IMsmError::get_ModuleTable
author: windows-sdk-content
description: The get_ModuleTable method retrieves the ModuleTable property of the Error object. This method returns the name of the table in the module that caused the error.
old-location: setup\imsmerror_get_moduletable.htm
tech.root: Msi
ms.assetid: c24145dc-0907-4916-bbec-f9e0ec7584db
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMsmError interface,get_ModuleTable method, IMsmError.get_ModuleTable, IMsmError::get_ModuleTable, _msi_get_moduletable_function, get_ModuleTable, get_ModuleTable method, get_ModuleTable method,IMsmError interface, mergemod/IMsmError::get_ModuleTable, setup.imsmerror_get_moduletable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
req.lib: 
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmError.get_ModuleTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mergemod.h
: 
- IMsmError.get_ModuleTable
: 
---

# IMsmError::get_ModuleTable


## -description


The 
<b>get_ModuleTable</b> method retrieves the 
<a href="https://msdn.microsoft.com/390f5889-d638-4c1c-b95c-76d38c934e7c">ModuleTable</a> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object. This method returns the name of the table in the module that caused the error.


## -parameters




### -param ErrorTable [out]

A pointer to a location in memory that is filled in with a <b>BSTR</b> value.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Table is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system was unable to allocate memory for the string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



The client is responsible for freeing the resulting string using <b>SysFreeString</b>.

The collection is empty if the values do not apply to the type of the error. You can determine the type of error by calling <a href="https://msdn.microsoft.com/733a5390-419d-414a-b50e-8400d179bfb6">IMsmError::get_Type</a>.




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

