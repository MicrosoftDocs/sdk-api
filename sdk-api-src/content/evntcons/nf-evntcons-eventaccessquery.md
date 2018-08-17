---
UID: NF:evntcons.EventAccessQuery
title: EventAccessQuery function
author: windows-sdk-content
description: Retrieves the permissions for the specified controller or provider.
old-location: etw\eventaccessquery_func.htm
old-project: etw
ms.assetid: 21c87137-0e8f-43d1-9dad-9f2b4fc591a3
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: EventAccessQuery, EventAccessQuery function [ETW], base.eventaccessquery_func, etw.eventaccessquery_func, evntcons/EventAccessQuery
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: evntcons.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: EVENTSECURITYOPERATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-eventing-controller-l1-1-0.dll
 - kernelbase.dll
api_name:
 - EventAccessQuery
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
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

For information on accessing the components of the security descriptor, see <a href="https://msdn.microsoft.com/a0839c49-09e9-4407-8702-051b88ef2231">Getting Information from an ACL</a>, the <a href="https://msdn.microsoft.com/8006c8bb-4976-463f-b074-a59c3bbab36b">GetSecurityDescriptorDacl</a>, <a href="https://msdn.microsoft.com/6bf59735-aaa3-4751-8c98-00cc197df4e5">GetSecurityDescriptorSacl</a>, and <a href="https://msdn.microsoft.com/5b5d8751-20d7-40a2-bd70-cfbe956aaa03">GetAce</a> functions, and the <a href="https://msdn.microsoft.com/980b8242-2ba2-469f-b834-da7d3fb22e14">ACE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/699bb165-680f-4d3b-8859-959f319ca4be">EventAccessControl</a>



<a href="https://msdn.microsoft.com/9f25f163-046c-41b0-82f9-0b214b74b87e">EventAccessRemove</a>
 

 

