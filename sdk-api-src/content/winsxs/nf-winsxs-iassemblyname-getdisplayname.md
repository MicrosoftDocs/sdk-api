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

# IAssemblyName::GetDisplayName


## -description


The <b>GetDisplayName</b> method gets a string representation of the side-by-side assembly name.


## -parameters




### -param szDisplayName [out]

A pointer to a buffer that receives the string value that contains the assembly name.


### -param pccDisplayName [in, out]

When calling this method, set this parameter to the size of the buffer specified by <b>szDisplayName</b>. Specify the size in characters and include the null terminator. When the method returns, the value of <i>pccDisplayName</i> is the size of the name returned.


### -param dwDisplayFlags [in]

One or more of the options of the <a href="https://msdn.microsoft.com/8f4c00b9-2684-44eb-9a68-bef6da87c396">ASM_DISPLAY_FLAGS</a> enumeration to specify which portions of the assembly's name to include in the string representation of the assembly name. The default for <i>dwDisplayFlags</i> is 0, which returns all portions of the assembly's display name.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_FALSE</dt>
</dl>
</td>
<td width="60%">
The method did not succeed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/304b8fb3-5d17-4af0-b070-450a40dc5cc9">IAssemblyName</a>
 

 

