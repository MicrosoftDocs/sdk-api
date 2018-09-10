---
UID: NF:chstrarr.CHStringArray.RemoveAll
title: CHStringArray::RemoveAll
author: windows-sdk-content
description: The RemoveAll method removes all the CHString members from this array.
old-location: wmi\chstringarray_removeall.htm
tech.root: WmiSdk
ms.assetid: be9df3fd-afa5-4f07-99cd-ddccdeaa3fd3
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],RemoveAll method, CHStringArray.RemoveAll, CHStringArray::RemoveAll, RemoveAll, RemoveAll method [Windows Management Instrumentation], RemoveAll method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_removeall, chstrarr/CHStringArray::RemoveAll, wmi.chstringarray_removeall
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
 - CHStringArray.RemoveAll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHStringArray::RemoveAll


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/en-us/library/Aa385304(v=VS.85).aspx">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/en-us/library/JJ152383(v=VS.85).aspx">MI APIs</a> should be used for all new 
    development.]

The <b>RemoveAll</b> method removes all the <a href="https://msdn.microsoft.com/en-us/library/Aa384937(v=VS.85).aspx">CHString</a> members from this array.


## -parameters






## -returns



This method does not return a value.




## -remarks



The <b>RemoveAll</b> method works on empty arrays.


#### Examples

The following code example shows the use of <b>CHStringArray::RemoveAll</b>.


```cpp
CHStringArray array;

array.Add( L"String 1" ); // Element 0
array.Add( L"String 2" ); // Element 1 
assert( array.GetSize() == 2 ); 
array.RemoveAll(); 
assert( array.GetSize() == 0 );
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa385304(v=VS.85).aspx">CHStringArray</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385361(v=VS.85).aspx">CHStringArray::FreeExtra</a>
 

 

