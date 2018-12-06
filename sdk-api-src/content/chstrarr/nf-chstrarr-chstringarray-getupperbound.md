---
UID: NF:chstrarr.CHStringArray.GetUpperBound
title: CHStringArray::GetUpperBound
author: windows-sdk-content
description: The GetUpperBound method gets the current upper bound of an array. Because array indexes are zero-based, this function returns a value that is one less than GetSize.
old-location: wmi\chstringarray_getupperbound.htm
tech.root: WmiSdk
ms.assetid: 77c200f9-c63b-4842-881f-5c077e4618b8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "?GetUpperBound@CHStringArray@@QBEHXZ, ?GetUpperBound@CHStringArray@@QEBAHXZ, CHStringArray interface [Windows Management Instrumentation],GetUpperBound method, CHStringArray.GetUpperBound, CHStringArray::GetUpperBound, GetUpperBound, GetUpperBound method [Windows Management Instrumentation], GetUpperBound method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_getupperbound, chstrarr/CHStringArray::GetUpperBound, wmi.chstringarray_getupperbound"
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
 - CHStringArray.GetUpperBound
 - ?GetUpperBound@CHStringArray@@QBEHXZ
 - ?GetUpperBound@CHStringArray@@QEBAHXZ
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHStringArray::GetUpperBound


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetUpperBound</b> method gets the current upper bound of an array. Because array indexes are zero-based, this function returns a value that is one less than <a href="https://msdn.microsoft.com/5db50c38-a9c7-4711-925e-291cebf2b6f1">GetSize</a>.


## -parameters






## -returns



If the <b>GetUpperBound</b> method is successful, it returns the upper bounds of this array. A value of -1 indicates that the array contains no elements.




## -see-also




<a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a>



<a href="https://msdn.microsoft.com/f5a0b8e6-b40a-4dc7-bf36-ec629e2899db">CHStringArray::Add</a>



<a href="https://msdn.microsoft.com/5db50c38-a9c7-4711-925e-291cebf2b6f1">CHStringArray::GetSize</a>



<a href="https://msdn.microsoft.com/9320b6b6-5253-419e-a293-3b9d030f5963">CHStringArray::SetSize</a>
 

 

