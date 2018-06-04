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

# NCryptQueryProtectionDescriptorName function


## -description


The <b>NCryptQueryProtectionDescriptorName</b> function retrieves the protection descriptor rule string associated with a registered descriptor display name.


## -parameters




### -param pwszName [in]

The registered display name for the protection descriptor. Register a name by calling the <a href="https://msdn.microsoft.com/DAB03CB2-630F-4BB3-93BD-06BE9126B1C4">NCryptRegisterProtectionDescriptorName</a> function.


### -param pwszDescriptorString [out]

A null-terminated Unicode string that contains the protection descriptor rule. Set this value to <b>NULL</b> and set the size of the descriptor string pointed to by <i>pcDescriptorString</i> argument to zero on your initial call to this function. For more information, see Remarks.


### -param pcDescriptorString [in, out]

Pointer to a variable that contains the number  of characters in the string retrieved in the <i>pwszDescriptorString</i> parameter. Set the variable to zero on your initial call to this function. For more information, see Remarks.


### -param dwFlags

Flag that specifies which registry hive to query for the registered name. This can be zero to look in the <b>HKEY_CURRENT_USER</b> hive or you can specify <b>NCRYPT_MACHINE_KEY_FLAG</b> to query the <b>HKEY_LOCAL_MACHINE</b> hive.


## -returns



Returns a status code that indicates the success or failure of the function. Possible return codes include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszName</i> parameter cannot be <b>NULL</b>, and the value pointed to by the parameter cannot be an empty string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter must be zero or <b>NCRYPT_MACHINE_KEY_FLAG</b>.

</td>
</tr>
</table>
 




## -remarks



To retrieve a protection descriptor rule string, you must call this function twice. The first time you call, set the <i>pwszDescriptorString</i> argument to <b>NULL</b> and the value pointed to by the <i>pcDescriptorString</i> argument to zero. Your first call retrieves the number of characters in the descriptor string. Use this number to allocate memory for the string and retrieve a pointer to the allocated buffer. To retrieve the string, call the function again using the pointer.




## -see-also




<a href="https://msdn.microsoft.com/591C7361-334E-4A65-8616-C0ED3BBC2297">CNG DPAPI Functions</a>



<a href="https://msdn.microsoft.com/DAB03CB2-630F-4BB3-93BD-06BE9126B1C4">NCryptRegisterProtectionDescriptorName</a>
 

 

