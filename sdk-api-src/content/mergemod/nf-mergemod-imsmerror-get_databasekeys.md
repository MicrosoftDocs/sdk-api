---
UID: NF:mergemod.IMsmError.get_DatabaseKeys
title: IMsmError::get_DatabaseKeys
author: windows-sdk-content
description: The get_DatabaseKeys method retrieves the DatabaseKeys property of the Error object. This method returns a pointer to a string collection containing the primary keys of the row in the database causing the error, one key per entry in the collection.
old-location: setup\imsmerror_get_databasekeys.htm
tech.root: MSI
ms.assetid: 7c256f03-208c-4adf-9b57-7648064f0dce
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMsmError interface,get_DatabaseKeys method, IMsmError.get_DatabaseKeys, IMsmError::get_DatabaseKeys, _msi_get_databasekeys_function, get_DatabaseKeys, get_DatabaseKeys method, get_DatabaseKeys method,IMsmError interface, mergemod/IMsmError::get_DatabaseKeys, setup.imsmerror_get_databasekeys
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
 - IMsmError.get_DatabaseKeys
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmError::get_DatabaseKeys


## -description


The 
<b>get_DatabaseKeys</b> method retrieves the 
<a href="https://msdn.microsoft.com/416a6cef-4c70-4c06-a8d2-801c9440e25a">DatabaseKeys</a> property of the <a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object. This method returns a pointer to a string collection containing the primary keys of the row in the database causing the error, one key per entry in the collection.


## -parameters




### -param ErrorKeys [out]

A pointer to a location in memory that receives a pointer to a string collection.


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
ErrorKeys is null.

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



The client is responsible for releasing the string collection when it is no longer required.

The collection is empty if the values do not apply to the type of the error. You can determine the type of error using <a href="https://msdn.microsoft.com/733a5390-419d-414a-b50e-8400d179bfb6">IMsmError::get_Type</a>.




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

