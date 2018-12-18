---
UID: NF:chstrarr.CHStringArray.GetAt(int)
title: CHStringArray::GetAt(int)
author: windows-sdk-content
description: Gets the array element at the specified index.
old-location: wmi\chstringarray_getat.htm
tech.root: WmiSdk
ms.assetid: a950bc1e-1c13-4880-aee7-9a4606979993
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],GetAt method, CHStringArray.GetAt, CHStringArray.GetAt(int), CHStringArray::GetAt, CHStringArray::GetAt(int), GetAt, GetAt method [Windows Management Instrumentation], GetAt method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_getat, chstrarr/CHStringArray::GetAt, wmi.chstringarray_getat
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


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetAt</b> method gets the array element at the specified index.


## -parameters




### -param nIndex

An integer index that is greater than or equal to zero (0), and less than or equal to the value returned by <a href="https://msdn.microsoft.com/77c200f9-c63b-4842-881f-5c077e4618b8">GetUpperBound</a>.

<div class="alert"><b>Note</b>  The <i>nIndex</i> parameter must be greater than or equal to 0. The debug version of the <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> library validates the bounds of <i>nIndex</i>; the release version does not.</div>
<div> </div>

## -returns



If the <b>GetAt</b> method is successful, it returns the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> pointer element currently at this index.




## -remarks



Passing a negative value or a value greater than the value returned by <a href="https://msdn.microsoft.com/77c200f9-c63b-4842-881f-5c077e4618b8">GetUpperBound</a> results in a failed assertion for debug builds.


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




<a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a>



<a href="https://msdn.microsoft.com/f5a0b8e6-b40a-4dc7-bf36-ec629e2899db">CHStringArray::Add</a>



<a href="https://msdn.microsoft.com/5431a9ae-e009-4457-87e4-bb91da8bfdb6">CHStringArray::ElementAt</a>



<a href="https://msdn.microsoft.com/b59a0c42-e753-43ff-bf39-279f0a8b9d2b">CHStringArray::GetData</a>



<a href="https://msdn.microsoft.com/709bed59-c154-4103-9d38-398945657ec6">CHStringArray::SetAt</a>



<a href="https://msdn.microsoft.com/93b10bef-908e-4c5e-aac3-b13051b2e7c9">CHStringArray::operator []</a>
 

 

