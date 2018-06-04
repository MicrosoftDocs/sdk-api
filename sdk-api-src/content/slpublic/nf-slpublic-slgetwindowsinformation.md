---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# SLGetWindowsInformation function


## -description


Retrieves the value portion of a name-value pair from the licensing policy of a software component.


## -parameters




### -param pwszValueName [in]

A pointer to a null-terminated string that contains the name associated with the value to retrieve.


### -param peDataType [out, optional]

A pointer to a value of the <a href="https://msdn.microsoft.com/245e79de-4823-4af9-926a-088e263cc802">SLDATATYPE</a> enumeration that specifies the type of data in the <i>ppbValue</i> buffer.


### -param pcbValue [out]

A pointer to the size, in bytes, of the <i>ppbValue</i> buffer.


### -param ppbValue [out]

A pointer to an array of <b>BYTE</b> pointers that specifies the value associated with the name specified by the <i>pwszValueName</i> parameter.

When you have finished using this array, free it by calling the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

This function can return the following values defined in Slerror.h.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_VALUE_NOT_FOUND</b></dt>
<dt>0xC004F012</dt>
</dl>
</td>
<td width="60%">
The specified name-value pair was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_RIGHT_NOT_GRANTED</b></dt>
<dt>0xC004F013</dt>
</dl>
</td>
<td width="60%">
The caller does not have the permissions necessary to call this function.

</td>
</tr>
</table>
 



