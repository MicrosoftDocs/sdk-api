---
UID: NF:chstrarr.CHStringArray.GetData
title: CHStringArray::GetData (chstrarr.h)
author: windows-sdk-content
description: The GetData method gains direct access to the elements in the array.
old-location: wmi\chstringarray_getdata.htm
tech.root: WmiSdk
ms.assetid: b59a0c42-e753-43ff-bf39-279f0a8b9d2b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],GetData method, CHStringArray.GetData, CHStringArray::GetData, GetData, GetData method [Windows Management Instrumentation], GetData method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_getdata, chstrarr/CHStringArray::GetData, wmi.chstringarray_getdata
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
 - CHStringArray.GetData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHStringArray::GetData


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetData</b> method gains direct access to the elements in the array.


## -parameters






## -returns



If the <b>GetData</b> method is successful, it returns a pointer to the array of <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> pointers.




## -remarks



If no elements are available,  <b>GetData</b> returns a <b>NULL</b> value.

Although direct access to the elements of an array can help you work more quickly, use caution when calling <b>GetData</b>. Any errors you make directly affect the elements of your array.




## -see-also




<a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a>



<a href="https://msdn.microsoft.com/5431a9ae-e009-4457-87e4-bb91da8bfdb6">CHStringArray::ElementAt</a>



<a href="https://msdn.microsoft.com/5ed54cc4-284b-4cd7-80c1-e9c5ff27c4bf">CHStringArray::FreeExtra</a>



<a href="https://msdn.microsoft.com/a950bc1e-1c13-4880-aee7-9a4606979993">CHStringArray::GetAt</a>



<a href="https://msdn.microsoft.com/709bed59-c154-4103-9d38-398945657ec6">CHStringArray::SetAt</a>



<a href="https://msdn.microsoft.com/9320b6b6-5253-419e-a293-3b9d030f5963">CHStringArray::SetSize</a>
 

 

