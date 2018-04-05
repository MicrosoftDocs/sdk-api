---
UID: NF:chstrarr.CHStringArray.SetSize
title: CHStringArray::SetSize method
author: windows-driver-content
description: The SetSize method establishes the size of an empty or existing array.
old-location: wmi\chstringarray_setsize.htm
old-project: WmiSdk
ms.assetid: 9320b6b6-5253-419e-a293-3b9d030f5963
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: CHStringArray, CHStringArray interface [Windows Management Instrumentation], SetSize method, CHStringArray::SetSize, SetSize method [Windows Management Instrumentation], SetSize method [Windows Management Instrumentation], CHStringArray interface, SetSize,CHStringArray.SetSize, _hmm_chstringarray_setsize, chstrarr/CHStringArray::SetSize, wmi.chstringarray_setsize
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
req.typenames: CF_SYNC_ROOT_STANDARD_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CHStringArray.SetSize
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHStringArray::SetSize method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetSize</b> method establishes the size of an empty or existing array.


## -parameters




### -param nNewSize

The new array size (number of elements). The value must be greater than or equal to 0 (zero).


### -param nGrowBy

The minimum number of element slots to allocate if a size increase is necessary.


## -returns



This method does not return a value.




## -remarks



The <b>SetSize</b> method allocates memory if necessary. If the new size is smaller than the old size, then the array is truncated, and all unused memory is released. For efficiency, call <b>SetSize</b> to set the size of the array before using it. This prevents the need to reallocate and copy the array each time an item is added.

The <i>nGrowBy</i> parameter affects internal memory allocation while the array is growing. Its use never affects the array size as reported by <a href="https://msdn.microsoft.com/5db50c38-a9c7-4711-925e-291cebf2b6f1">GetSize</a> and <a href="https://msdn.microsoft.com/77c200f9-c63b-4842-881f-5c077e4618b8">GetUpperBound</a>.


#### Examples

See the example for <a href="https://msdn.microsoft.com/b59a0c42-e753-43ff-bf39-279f0a8b9d2b">CHStringArray::GetData</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a>



<a href="https://msdn.microsoft.com/b59a0c42-e753-43ff-bf39-279f0a8b9d2b">CHStringArray::GetData</a>



<a href="https://msdn.microsoft.com/5db50c38-a9c7-4711-925e-291cebf2b6f1">CHStringArray::GetSize</a>



<a href="https://msdn.microsoft.com/77c200f9-c63b-4842-881f-5c077e4618b8">CHStringArray::GetUpperBound</a>
 

 

