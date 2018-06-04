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

# SetShellNext function


## -description


<p class="CCE_Message">[This function is available for use in the Windows XP  operating system.  It may be altered or unavailable in subsequent versions.]

Sets the <b>ShellNext</b> registry key with the specified value.


## -parameters




### -param szShellNext [in]

The string value.
The length is expected to be less than or equal to <b>MAX_PATH</b> characters.


## -returns



This function can return one of these values.


This function returns one of the following values.



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
The call is successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>szShellNext</i> contains a <b>NULL</b> pointer or the string is zero in length.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/81960d59-3de3-4d86-948e-939c59073bb1">CheckConnectionWizard</a>
 

 

