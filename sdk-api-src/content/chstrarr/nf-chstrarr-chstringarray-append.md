---
UID: NF:chstrarr.CHStringArray.Append
title: CHStringArray::Append (chstrarr.h)
author: windows-sdk-content
description: The Append method adds the contents of another array to the end of the given array.
old-location: wmi\chstringarray_append.htm
tech.root: WmiSdk
ms.assetid: c37df3d4-9b0b-4ed3-ab51-407f26203578
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Append, Append method [Windows Management Instrumentation], Append method [Windows Management Instrumentation],CHStringArray interface, CHStringArray interface [Windows Management Instrumentation],Append method, CHStringArray.Append, CHStringArray::Append, _hmm_chstringarray_append, chstrarr/CHStringArray::Append, wmi.chstringarray_append
ms.topic: method
f1_keywords: 
 - "chstrarr/CHStringArray.Append"
dev_langs:
 - c++
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
 - CHStringArray.Append
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CHStringArray::Append


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>Append</b> method adds the contents of another array to the end of the given array.


## -parameters




### -param src [ref]

Source of the elements to be appended to the array.


## -returns



If the <b>Append</b> method is successful, it returns the index of the first appended element.




## -remarks



If necessary,  <b>Append</b> can allocate extra memory to accommodate the elements appended to the array.


#### Examples

The following code example shows the use of <b>CHStringArray::Append</b>.


```cpp
CHStringArray myArray1, myArray2;
int idx, size;

// Add elements to the second array.
myArray2.Add( L"String 2" );
myArray2.Add( L"String 3" );

// Add elements to the first array and also append the second array. 
myArray1.Add( L"String 1" );
myArray1.Append( myArray2 );

size = myArray1.GetSize();
for (idx=0; idx<size; idx++)
   printf("[%d]: %S\n", idx, myArray1[idx]);
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a>



<a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-add">CHStringArray::Add</a>



<a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-copy">CHStringArray::Copy</a>
 

 

