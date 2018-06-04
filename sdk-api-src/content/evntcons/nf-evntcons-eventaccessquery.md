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

# EventAccessQuery function


## -description



		Retrieves the permissions for the specified controller or provider.
		
		
	
	


## -parameters




### -param Guid [in]

GUID that uniquely identifies the provider or session.


### -param Buffer [in, out]

Application-allocated buffer that will contain the security descriptor of the controller or provider.


### -param BufferSize [in, out]

Size of the security descriptor buffer, in bytes. If the function succeeds, this parameter receives the size of the buffer used. If the buffer is too small, the function returns ERROR_MORE_DATA and this parameter receives the required buffer size. If the buffer size is zero on input, no data is returned in the buffer and this parameter receives the required buffer size.


## -returns



Returns ERROR_SUCCESS if successful.

The function returns the following return code if an error occurs:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small to receive the security descriptor. Reallocate the buffer using the size returned in <i>BufferSize</i>.

</td>
</tr>
</table>
 




## -remarks



If the GUID does not exist in the registry, ETW returns the default permissions for a provider or controller. For details on specifying the GUID in the registry, see <a href="https://msdn.microsoft.com/699bb165-680f-4d3b-8859-959f319ca4be">EventAccessControl</a>.

For information on accessing the components of the security descriptor, see <a href="https://msdn.microsoft.com/a0839c49-09e9-4407-8702-051b88ef2231">Getting Information from an ACL</a>, the <a href="https://msdn.microsoft.com/8006c8bb-4976-463f-b074-a59c3bbab36b">GetSecurityDescriptorDacl</a>, <a href="https://msdn.microsoft.com/6bf59735-aaa3-4751-8c98-00cc197df4e5">GetSecurityDescriptorSacl</a>, and <a href="https://msdn.microsoft.com/5b5d8751-20d7-40a2-bd70-cfbe956aaa03">GetAce</a> functions, and the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538844">ACE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/699bb165-680f-4d3b-8859-959f319ca4be">EventAccessControl</a>



<a href="https://msdn.microsoft.com/9f25f163-046c-41b0-82f9-0b214b74b87e">EventAccessRemove</a>
 

 

