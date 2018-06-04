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

# CHStringArray::Copy


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>Copy</b> method overwrites the elements of the given array with the elements of another array.


## -parameters




### -param src [ref]

Source of the elements to be copied to the array.


## -returns



This method does not return a value.




## -remarks



The <b>Copy</b> method does not free memory, but it allocates extra memory to accommodate the elements copied to the array.


#### Examples

The following code example shows the use of <b>CHStringArray::Copy</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CHStringArray a1, a2;
int idx, size;

a1.Add( L"String 1" );
a1.Add( L"String 2" );
a2.Add( L"String 5" );

size = a1.GetSize();
for (idx=0; idx&lt;size; idx++)
   printf("[%d]: %S\n", idx, a1[idx]);

a1.Copy(a2);
size = a1.GetSize();
for (idx=0; idx&lt;size; idx++)
   printf("[%d]: %S\n", idx, a1[idx]);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a>



<a href="https://msdn.microsoft.com/f5a0b8e6-b40a-4dc7-bf36-ec629e2899db">CHStringArray::Add</a>



<a href="https://msdn.microsoft.com/c37df3d4-9b0b-4ed3-ab51-407f26203578">CHStringArray::Append</a>
 

 

