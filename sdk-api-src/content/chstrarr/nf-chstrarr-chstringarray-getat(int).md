---
UID: NF:chstrarr.CHStringArray.GetAt(int)
title: CHStringArray::GetAt(int)
author: windows-sdk-content
description: Gets the array element at the specified index.
old-location: wmi\chstringarray_getat.htm
tech.root: WmiSdk
ms.assetid: a950bc1e-1c13-4880-aee7-9a4606979993
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],GetAt method, CHStringArray.GetAt, CHStringArray.GetAt(int), CHStringArray::GetAt, CHStringArray::GetAt(int), GetAt, GetAt method [Windows Management Instrumentation], GetAt method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_getat, chstrarr/CHStringArray::GetAt, wmi.chstringarray_getat
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
 - CHStringArray.GetAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHStringArray::GetAt(int)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/en-us/library/Aa385304(v=VS.85).aspx">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/en-us/library/JJ152383(v=VS.85).aspx">MI APIs</a> should be used for all new 
    development.]

The <b>GetAt</b> method gets the array element at the specified index.


## -parameters




### -param nIndex

An integer index that is greater than or equal to zero (0), and less than or equal to the value returned by <a href="https://msdn.microsoft.com/en-us/library/Aa385377(v=VS.85).aspx">GetUpperBound</a>.

<div class="alert"><b>Note</b>  The <i>nIndex</i> parameter must be greater than or equal to 0. The debug version of the <a href="https://msdn.microsoft.com/en-us/library/Aa385304(v=VS.85).aspx">CHStringArray</a> library validates the bounds of <i>nIndex</i>; the release version does not.</div>
<div> </div>

## -returns



If the <b>GetAt</b> method is successful, it returns the <a href="https://msdn.microsoft.com/en-us/library/Aa384937(v=VS.85).aspx">CHString</a> pointer element currently at this index.




## -remarks



Passing a negative value or a value greater than the value returned by <a href="https://msdn.microsoft.com/en-us/library/Aa385377(v=VS.85).aspx">GetUpperBound</a> results in a failed assertion for debug builds.


#### Examples

The following code example shows the use of <b>CHStringArray::GetAt</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CHStringArray array;

array.Add( L"String 1" ); // Element 0 
array.Add( L"String 2" ); // Element 1 
assert( array.GetAt( 0 ) == "String 1" );</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa385304(v=VS.85).aspx">CHStringArray</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385329(v=VS.85).aspx">CHStringArray::Add</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385356(v=VS.85).aspx">CHStringArray::ElementAt</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385367(v=VS.85).aspx">CHStringArray::GetData</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385402(v=VS.85).aspx">CHStringArray::SetAt</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385421(v=VS.85).aspx">CHStringArray::operator []</a>
 

 

