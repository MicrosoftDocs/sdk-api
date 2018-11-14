---
UID: NF:chstrarr.CHStringArray.Copy
title: CHStringArray::Copy
author: windows-sdk-content
description: The Copy method overwrites the elements of the given array with the elements of another array.
old-location: wmi\chstringarray_copy.htm
tech.root: WmiSdk
ms.assetid: 9598340f-c315-4c93-bc8a-2b7c1eaf5a35
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],Copy method, CHStringArray.Copy, CHStringArray::Copy, Copy, Copy method [Windows Management Instrumentation], Copy method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_copy, chstrarr/CHStringArray::Copy, wmi.chstringarray_copy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: chstrarr.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHStringArray.Copy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- chstrarr.h
: 
- CHStringArray.Copy
: 
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
 

 

