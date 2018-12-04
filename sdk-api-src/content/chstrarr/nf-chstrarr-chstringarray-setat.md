---
UID: NF:chstrarr.CHStringArray.SetAt
title: CHStringArray::SetAt
author: windows-sdk-content
description: The SetAt method sets the array element at the specified index.
old-location: wmi\chstringarray_setat.htm
tech.root: WmiSdk
ms.assetid: 709bed59-c154-4103-9d38-398945657ec6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],SetAt method, CHStringArray.SetAt, CHStringArray::SetAt, SetAt, SetAt method [Windows Management Instrumentation], SetAt method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_setat, chstrarr/CHStringArray::SetAt, wmi.chstringarray_setat
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
 - CHStringArray.SetAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHStringArray::SetAt


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetAt</b> method sets the array element at the specified index.


## -parameters




### -param nIndex

An integer index that is greater than or equal to zero and less than or equal to the value returned by <a href="https://msdn.microsoft.com/77c200f9-c63b-4842-881f-5c077e4618b8">GetUpperBound</a>.


### -param newElement

The object pointer that is inserted in this array. A <b>NULL</b> value is allowed.


## -returns



This method does not return a value.




## -remarks



The <b>SetAt</b> method does not cause the array to increase. Use <a href="https://msdn.microsoft.com/49cc7e6f-2d15-4756-bffd-e21f38b8ce8b">SetAtGrow</a> if you want the array to increase automatically.

You must ensure that your index value represents a valid position in the array.


#### Examples

The following code example shows the use of <b>CHStringArray::SetAt</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CHStringArray array;

array.Add( L"String 1" ); // Element 0
array.Add( L"String 2" ); // Element 1
array.SetAt( 0, L"String 3" );  // Replace element 0.
assert( array[0] == "String 3" );</pre>
</td>
</tr>
</table></span></div>
The following  example results in a <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> with two elements.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    [0] = String 3
    [1] = String 2</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a>



<a href="https://msdn.microsoft.com/f5a0b8e6-b40a-4dc7-bf36-ec629e2899db">CHStringArray::Add</a>



<a href="https://msdn.microsoft.com/5431a9ae-e009-4457-87e4-bb91da8bfdb6">CHStringArray::ElementAt</a>



<a href="https://msdn.microsoft.com/a950bc1e-1c13-4880-aee7-9a4606979993">CHStringArray::GetAt</a>



<a href="https://msdn.microsoft.com/b59a0c42-e753-43ff-bf39-279f0a8b9d2b">CHStringArray::GetData</a>



<a href="https://msdn.microsoft.com/93b10bef-908e-4c5e-aac3-b13051b2e7c9">CHStringArray::operator []</a>
 

 

