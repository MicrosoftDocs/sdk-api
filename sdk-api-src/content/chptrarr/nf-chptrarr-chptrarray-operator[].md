---
UID: NF:chptrarr.CHPtrArray.operator[]
title: CHPtrArray::operator[] method
author: windows-driver-content
description: The CHPtrArray::operator[] subscript operators get the element at the specified index. You can use this function in place of the CHPtrArray::GetAt method.
old-location: wmi\chptrarray__operator_brackets.htm
old-project: WmiSdk
ms.assetid: 7005130a-bc0d-4058-aba2-d12ed50255cd
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: CHPtrArray, CHPtrArray interface [Windows Management Instrumentation], operator [] method, CHPtrArray::operator [], CHPtrArray::operator[], chptrarr/CHPtrArray::operator [], operator [] method [Windows Management Instrumentation], operator [] method [Windows Management Instrumentation], CHPtrArray interface, operator[],CHPtrArray.operator[], wmi.chptrarray__operator_brackets
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
-	CHPtrArray.operator []
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHPtrArray::operator[] method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/507c8262-c5e8-470e-be89-566ae732946d">CHPtrArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The CHPtrArray::operator[] subscript operators get the element at the specified index. You can use this  function in place of the <a href="https://msdn.microsoft.com/7c2f029f-22a1-4433-971e-35ce48c004e0">CHPtrArray::GetAt</a> method.


## -parameters




### -param nIndex

Zero-based index of a character in the string.


## -returns



The subscript operators return the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHPtrArray</a> pointer element currently at this index.




## -remarks



You can use the first operator, which calls for arrays that are not <b>const</b>, on either the right (r-value) or the left (l-value) side of an assignment statement. The second, which calls for <b>const</b> arrays, can be used only on the right.




## -see-also




<a href="https://msdn.microsoft.com/507c8262-c5e8-470e-be89-566ae732946d">CHPtrArray</a>



<a href="https://msdn.microsoft.com/d2414a72-3435-4035-bcd9-b3ec87f5709c">Provider Framework Utility Classes</a>
 

 

