---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IFillLockBytes::SetFillSize


## -description



			The 
<b>SetFillSize</b> method sets the expected size of the byte array.


## -parameters




### -param ulSize






#### - uISize [in]

Size in bytes of the byte array object that is to be filled in subsequent calls to 
<a href="https://msdn.microsoft.com/3f25c48f-85a4-4778-b262-ad0c52cb1ac9">IFillLockBytes::FillAppend</a>.


## -returns




						This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL.




## -remarks



If 
<b>SetFillSize</b> has not been called, any call to 
<a href="https://msdn.microsoft.com/0478d6f0-65c4-445b-946a-692f2373e8f1">ILockBytes::ReadAt</a> that attempts to access data that has not yet been written using 
<a href="https://msdn.microsoft.com/3f25c48f-85a4-4778-b262-ad0c52cb1ac9">IFillLockBytes::FillAppend</a> or 
<a href="https://msdn.microsoft.com/d378d87b-e081-4950-b87b-9b1ad6dfb29d">IFillLockBytes::FillAt</a> will return a new error message, E_PENDING. After 
<b>SetFillSize</b> has been called, any call to 
<b>ReadAt</b> that attempts to access data beyond the current size, as set by 
<b>SetFillSize</b>, returns E_FAIL instead of E_PENDING.




## -see-also




<a href="https://msdn.microsoft.com/3f25c48f-85a4-4778-b262-ad0c52cb1ac9">IFillLockBytes::FillAppend</a>



<a href="https://msdn.microsoft.com/d378d87b-e081-4950-b87b-9b1ad6dfb29d">IFillLockBytes::FillAt</a>



<a href="https://msdn.microsoft.com/0478d6f0-65c4-445b-946a-692f2373e8f1">ILockBytes::ReadAt</a>
 

 

