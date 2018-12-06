---
UID: NF:chptrarr.CHPtrArray.GetAt
title: CHPtrArray::GetAt
author: windows-sdk-content
description: The GetAt method accesses an element in a CHPtrArray array.
old-location: wmi\chptrarray_getat.htm
tech.root: WmiSdk
ms.assetid: 7c2f029f-22a1-4433-971e-35ce48c004e0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "?GetAt@CHPtrArray@@QBEPAXH@Z, CHPtrArray interface [Windows Management Instrumentation],GetAt method, CHPtrArray.GetAt, CHPtrArray::GetAt, GetAt, GetAt method [Windows Management Instrumentation], GetAt method [Windows Management Instrumentation],CHPtrArray interface, chptrarr/CHPtrArray::GetAt, wmi.chptrarray_getat"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: chptrarr.h
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
 - CHPtrArray.GetAt
 - ?GetAt@CHPtrArray@@QBEPAXH@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHPtrArray::GetAt


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/507c8262-c5e8-470e-be89-566ae732946d">CHPtrArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetAt</b> method accesses an element in a <a href="https://msdn.microsoft.com/507c8262-c5e8-470e-be89-566ae732946d">CHPtrArray</a> array.


## -parameters




### -param nIndex

An integer index that is greater than or equal to zero (0), and less than or equal to the upper bound.


## -returns



If the <b>GetAt</b> method is successful, it returns the <a href="https://msdn.microsoft.com/507c8262-c5e8-470e-be89-566ae732946d">CHPtrArray</a> pointer element currently at this index.




## -see-also




<a href="https://msdn.microsoft.com/507c8262-c5e8-470e-be89-566ae732946d">CHPtrArray</a>



<a href="https://msdn.microsoft.com/d2414a72-3435-4035-bcd9-b3ec87f5709c">Provider Framework Utility Classes</a>
 

 

