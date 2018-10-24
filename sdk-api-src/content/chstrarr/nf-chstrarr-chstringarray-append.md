---
UID: NF:chstrarr.CHStringArray.Append
title: CHStringArray::Append
author: windows-sdk-content
description: The Append method adds the contents of another array to the end of the given array.
old-location: wmi\chstringarray_append.htm
tech.root: WmiSdk
ms.assetid: c37df3d4-9b0b-4ed3-ab51-407f26203578
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: Append, Append method [Windows Management Instrumentation], Append method [Windows Management Instrumentation],CHStringArray interface, CHStringArray interface [Windows Management Instrumentation],Append method, CHStringArray.Append, CHStringArray::Append, _hmm_chstringarray_append, chstrarr/CHStringArray::Append, wmi.chstringarray_append
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
 - CHStringArray.Append
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHStringArray::Append


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
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




<a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a>



<a href="https://msdn.microsoft.com/f5a0b8e6-b40a-4dc7-bf36-ec629e2899db">CHStringArray::Add</a>



<a href="https://msdn.microsoft.com/9598340f-c315-4c93-bc8a-2b7c1eaf5a35">CHStringArray::Copy</a>
 

 

