---
UID: NF:chstrarr.CHStringArray.InsertAt(int,CHStringArray)
title: CHStringArray::InsertAt(int,CHStringArray) (chstrarr.h)
author: windows-sdk-content
description: The InsertAt method inserts all of the elements of another CHStringArray array at the index specified by nStartIndex.
old-location: wmi\chstringarray_insertat_int__chstringarray__.htm
tech.root: WmiSdk
ms.assetid: 4aab5eb2-0b6d-4ffc-b627-a35c0696c7cc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CHStringArray.InsertAt, CHStringArray.InsertAt(int,CHStringArray), CHStringArray::InsertAt, CHStringArray::InsertAt methods [Windows Management Instrumentation], CHStringArray::InsertAt(int,CHStringArray), InsertAt, chstrarr/CHStringArray::InsertAt, wmi.insertat_method_in_class_chstringarray
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
 - CHStringArray.InsertAt(int, CHStringArray*)
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHStringArray::InsertAt(int,CHStringArray)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>InsertAt</b> method inserts  all of the elements of another <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> array at the index specified by <i>nStartIndex</i>.


## -parameters




### -param nStartIndex

Type: <b>int</b>

An integer index that can be greater than the value returned by <a href="https://msdn.microsoft.com/77c200f9-c63b-4842-881f-5c077e4618b8">GetUpperBound</a>.


### -param pNewArray

Type: <b>CHStringArray*</b>

Pointer to another <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> that contains the elements to be inserted into this array.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a>



<a href="https://msdn.microsoft.com/f5a0b8e6-b40a-4dc7-bf36-ec629e2899db">CHStringArray::Add</a>



<a href="https://msdn.microsoft.com/b7555074-4f9a-46be-b321-f16e00663c32">CHStringArray::RemoveAt</a>



<a href="https://msdn.microsoft.com/709bed59-c154-4103-9d38-398945657ec6">CHStringArray::SetAt</a>
 

 

