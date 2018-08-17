---
UID: NF:chstrarr.CHStringArray.SetAt
title: CHStringArray::SetAt
author: windows-sdk-content
description: The SetAt method sets the array element at the specified index.
old-location: wmi\chstringarray_setat.htm
old-project: WmiSdk
ms.assetid: 709bed59-c154-4103-9d38-398945657ec6
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],SetAt method, CHStringArray.SetAt, CHStringArray::SetAt, SetAt, SetAt method [Windows Management Instrumentation], SetAt method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_setat, chstrarr/CHStringArray::SetAt, wmi.chstringarray_setat
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
 - CHStringArray.SetAt
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHStringArray::SetAt


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/en-us/library/Aa385304(v=VS.85).aspx">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/en-us/library/JJ152383(v=VS.85).aspx">MI APIs</a> should be used for all new 
    development.]

The <b>SetAt</b> method sets the array element at the specified index.


## -parameters




### -param nIndex

An integer index that is greater than or equal to zero and less than or equal to the value returned by <a href="https://msdn.microsoft.com/en-us/library/Aa385377(v=VS.85).aspx">GetUpperBound</a>.


### -param newElement

The object pointer that is inserted in this array. A <b>NULL</b> value is allowed.


## -returns



This method does not return a value.




## -remarks



The <b>SetAt</b> method does not cause the array to increase. Use <a href="https://msdn.microsoft.com/en-us/library/Aa385409(v=VS.85).aspx">SetAtGrow</a> if you want the array to increase automatically.

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
The following  example results in a <a href="https://msdn.microsoft.com/en-us/library/Aa385304(v=VS.85).aspx">CHStringArray</a> with two elements.

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




<a href="https://msdn.microsoft.com/en-us/library/Aa385304(v=VS.85).aspx">CHStringArray</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385329(v=VS.85).aspx">CHStringArray::Add</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385356(v=VS.85).aspx">CHStringArray::ElementAt</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385363(v=VS.85).aspx">CHStringArray::GetAt</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385367(v=VS.85).aspx">CHStringArray::GetData</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385421(v=VS.85).aspx">CHStringArray::operator []</a>
 

 

