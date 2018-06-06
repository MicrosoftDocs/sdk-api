---
UID: NF:chstrarr.CHStringArray.ElementAt
title: CHStringArray::ElementAt
author: windows-sdk-content
description: The ElementAt method returns a temporary reference to the element pointer within the array.
old-location: wmi\chstringarray_elementat.htm
old-project: WmiSdk
ms.assetid: 5431a9ae-e009-4457-87e4-bb91da8bfdb6
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],ElementAt method, CHStringArray.ElementAt, CHStringArray::ElementAt, ElementAt, ElementAt method [Windows Management Instrumentation], ElementAt method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_elementat, chstrarr/CHStringArray::ElementAt, wmi.chstringarray_elementat
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CONFLICT_DETAILS_W, *PCONFLICT_DETAILS_W
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHStringArray.ElementAt
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHStringArray::ElementAt


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>ElementAt</b> method returns a temporary reference to the element pointer within the array.


## -parameters




### -param nIndex

An integer index that is greater than or equal to zero and less than or equal to the value returned by <a href="https://msdn.microsoft.com/77c200f9-c63b-4842-881f-5c077e4618b8">GetUpperBound</a>.


## -returns



If the <b>ElementAt</b> method is successful, it returns a reference to the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string at the <i>nIndex</i> position in the <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> array.




## -remarks



Use the <b>ElementAt</b> method to implement the left-side assignment operator for arrays. This is an advanced method, which you should use only to implement special array operators.


#### Examples

See the example for <a href="https://msdn.microsoft.com/5db50c38-a9c7-4711-925e-291cebf2b6f1">CHStringArray::GetSize</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a>



<a href="https://msdn.microsoft.com/a950bc1e-1c13-4880-aee7-9a4606979993">CHStringArray::GetAt</a>



<a href="https://msdn.microsoft.com/b59a0c42-e753-43ff-bf39-279f0a8b9d2b">CHStringArray::GetData</a>



<a href="https://msdn.microsoft.com/709bed59-c154-4103-9d38-398945657ec6">CHStringArray::SetAt</a>
 

 

