---
UID: NF:chstrarr.CHStringArray.InsertAt(int,LPCWSTR,int)
title: CHStringArray::InsertAt(int,LPCWSTR,int)
author: windows-sdk-content
description: The InsertAt method inserts an element (or multiple copies of an element) at a specified index in an array. The element at the specified index and all elements to its right shift up by one index value for each copy inserted.
old-location: wmi\chstringarray_insertat_int__lpcwstr__int_.htm
tech.root: WmiSdk
ms.assetid: 0c8e519a-ace8-47ce-a538-138e8f9720a6
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],InsertAt(int,LPCWSTR,int) method, CHStringArray.InsertAt, CHStringArray.InsertAt(int,LPCWSTR,int), CHStringArray::InsertAt, CHStringArray::InsertAt(int,LPCWSTR,int), InsertAt, InsertAt(int,LPCWSTR,int) method [Windows Management Instrumentation], InsertAt(int,LPCWSTR,int) method [Windows Management Instrumentation],CHStringArray interface, chstrarr/CHStringArray::InsertAt(int,LPCWSTR,int), wmi.chstringarray_insertat_int__lpcwstr__int_
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
 - CHStringArray.InsertAt(int, LPCWSTR, int)
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHStringArray::InsertAt(int,LPCWSTR,int)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>InsertAt</b> method inserts an element (or multiple copies of an element) at a specified index in an array. The element at the specified index and all elements to its right shift up by one index value for each copy inserted.


## -parameters




### -param nIndex

An integer index that can be greater than the value returned by <a href="https://msdn.microsoft.com/77c200f9-c63b-4842-881f-5c077e4618b8">GetUpperBound</a>.


### -param newElement

The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> pointer to be placed in this array.


### -param nCount

The number of times this element should be inserted. The default is 1.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a>



<a href="https://msdn.microsoft.com/f5a0b8e6-b40a-4dc7-bf36-ec629e2899db">CHStringArray::Add</a>



<a href="https://msdn.microsoft.com/b7555074-4f9a-46be-b321-f16e00663c32">CHStringArray::RemoveAt</a>



<a href="https://msdn.microsoft.com/709bed59-c154-4103-9d38-398945657ec6">CHStringArray::SetAt</a>
 

 

