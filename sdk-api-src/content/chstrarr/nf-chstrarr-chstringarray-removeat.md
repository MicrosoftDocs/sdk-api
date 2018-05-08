---
UID: NF:chstrarr.CHStringArray.RemoveAt
title: CHStringArray::RemoveAt
author: windows-driver-content
description: The RemoveAt method removes one or more elements starting at a specified index in an array.
old-location: wmi\chstringarray_removeat.htm
old-project: WmiSdk
ms.assetid: b7555074-4f9a-46be-b321-f16e00663c32
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],RemoveAt method, CHStringArray.RemoveAt, CHStringArray::RemoveAt, RemoveAt, RemoveAt method [Windows Management Instrumentation], RemoveAt method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_removeat, chstrarr/CHStringArray::RemoveAt, wmi.chstringarray_removeat
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
req.typenames: CF_SYNC_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CHStringArray.RemoveAt
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHStringArray::RemoveAt


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>RemoveAt</b> method removes one or more elements starting at a specified index in an array.


## -parameters




### -param nIndex

An integer index that is greater than or equal to zero and less than or equal to the value returned by <a href="https://msdn.microsoft.com/77c200f9-c63b-4842-881f-5c077e4618b8">GetUpperBound</a>.


### -param nCount

The number of elements to remove. The default is 1 (one).


## -returns



This method does not return a value.




## -remarks



In the process of removing elements,  <b>RemoveAt</b> shifts down all the elements located above the elements that are removed. This method decrements the upper bound of the array but does not free memory.


#### Examples

The following code example shows the use of <b>CHStringArray::RemoveAt</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CHStringArray array;

array.Add( L"String 1" ); // Element 0
array.Add( L"String 2" ); // Element 1
array.RemoveAt( 0 );  // Element 1 moves to 0.
assert ( array[0] == L"String 2" );</pre>
</td>
</tr>
</table></span></div>
The results from this program are as follows.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>[0] = String 2</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a>



<a href="https://msdn.microsoft.com/f5a0b8e6-b40a-4dc7-bf36-ec629e2899db">CHStringArray::Add</a>



<a href="https://msdn.microsoft.com/a950bc1e-1c13-4880-aee7-9a4606979993">CHStringArray::GetAt</a>



<a href="https://msdn.microsoft.com/1d6355bc-7df2-4aa3-8e47-0239d726ed7d">CHStringArray::InsertAt</a>
 

 

