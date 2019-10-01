---
UID: NF:chstrarr.CHStringArray.RemoveAt
title: CHStringArray::RemoveAt (chstrarr.h)
author: windows-sdk-content
description: The RemoveAt method removes one or more elements starting at a specified index in an array.
old-location: wmi\chstringarray_removeat.htm
tech.root: WmiSdk
ms.assetid: b7555074-4f9a-46be-b321-f16e00663c32
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],RemoveAt method, CHStringArray.RemoveAt, CHStringArray::RemoveAt, RemoveAt, RemoveAt method [Windows Management Instrumentation], RemoveAt method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_removeat, chstrarr/CHStringArray::RemoveAt, wmi.chstringarray_removeat
ms.topic: method
f1_keywords: 
 - "chstrarr/CHStringArray.RemoveAt"
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
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHStringArray.RemoveAt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CHStringArray::RemoveAt


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>RemoveAt</b> method removes one or more elements starting at a specified index in an array.


## -parameters




### -param nIndex

An integer index that is greater than or equal to zero and less than or equal to the value returned by <a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getupperbound">GetUpperBound</a>.


### -param nCount

The number of elements to remove. The default is 1 (one).


## -returns



This method does not return a value.




## -remarks



In the process of removing elements,  <b>RemoveAt</b> shifts down all the elements located above the elements that are removed. This method decrements the upper bound of the array but does not free memory.


#### Examples

The following code example shows the use of <b>CHStringArray::RemoveAt</b>.


```cpp
CHStringArray array;

array.Add( L"String 1" ); // Element 0
array.Add( L"String 2" ); // Element 1
array.RemoveAt( 0 );  // Element 1 moves to 0.
assert ( array[0] == L"String 2" );
```


The results from this program are as follows.


```cpp
[0] = String 2
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a>



<a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-add">CHStringArray::Add</a>



<a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getat(int)">CHStringArray::GetAt</a>



<a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray)">CHStringArray::InsertAt</a>
 

 

