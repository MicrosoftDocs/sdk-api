---
UID: NF:chstrarr.CHStringArray.Copy
title: CHStringArray::Copy
author: windows-sdk-content
description: The Copy method overwrites the elements of the given array with the elements of another array.
old-location: wmi\chstringarray_copy.htm
old-project: WmiSdk
ms.assetid: 9598340f-c315-4c93-bc8a-2b7c1eaf5a35
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],Copy method, CHStringArray.Copy, CHStringArray::Copy, Copy, Copy method [Windows Management Instrumentation], Copy method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_copy, chstrarr/CHStringArray::Copy, wmi.chstringarray_copy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: chstrarr.h
req.include-header: FwCommon.h
req.redist: 
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
tech.root: 
req.typenames: CONFLICT_DETAILS_W, *PCONFLICT_DETAILS_W
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
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHStringArray::Copy


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/en-us/library/Aa385304(v=VS.85).aspx">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/en-us/library/JJ152383(v=VS.85).aspx">MI APIs</a> should be used for all new 
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




<a href="https://msdn.microsoft.com/en-us/library/Aa385304(v=VS.85).aspx">CHStringArray</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385329(v=VS.85).aspx">CHStringArray::Add</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385337(v=VS.85).aspx">CHStringArray::Append</a>
 

 

