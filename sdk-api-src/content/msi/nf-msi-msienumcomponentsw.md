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

# MsiEnumComponentsW function


## -description


The 
<b>MsiEnumComponents</b> function enumerates the installed components for all products. This function retrieves one component code each time it is called.


## -parameters




### -param iComponentIndex [in]

Specifies the index of the component to retrieve. This parameter should be zero for the first call to the 
<b>MsiEnumComponents</b> function and then incremented for subsequent calls. Because components are not ordered, any new component has an arbitrary index. This means that the function can return components in any order.


### -param lpComponentBuf [out]

Pointer to a buffer that receives the component code. This buffer must be 39 characters long. The first 38 characters are for the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>, and the last character is for the terminating null character.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration data is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no components to return.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system does not have enough memory to complete the operation. Available with Windows Server 2003.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
A value was enumerated.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



To enumerate components, an application should initially call the 
<b>MsiEnumComponents</b> function with the <i>iComponentIndex</i> parameter set to zero. The application should then increment the <i>iComponentIndex</i> parameter and call 
<b>MsiEnumComponents</b> until there are no more components (that is, until the function returns ERROR_NO_MORE_ITEMS).

When making multiple calls to 
<b>MsiEnumComponents</b> to enumerate all of the product's components, each call should be made from the same thread.




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">System Status Functions</a>
 

 

