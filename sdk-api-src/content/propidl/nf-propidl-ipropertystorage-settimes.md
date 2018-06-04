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

# IPropertyStorage::SetTimes


## -description



			The <b>SetTimes</b> method sets the modification, access, and creation times of this property set, if supported by the implementation. Not all implementations support all these time values.


## -parameters




### -param pctime [in]

Pointer to the new creation time for the property set. May be <b>NULL</b>, indicating that this time is not to be modified by this call.


### -param patime [in]

Pointer to the new access time for the property set. May be <b>NULL</b>, indicating that this time is not to be modified by this call.


### -param pmtime [in]

Pointer to the new modification time for the property set. May be <b>NULL</b>, indicating that this time is not to be modified by this call.


## -returns




						This method supports the standard return value E_UNEXPECTED, in addition to the following:




## -remarks



Sets the modification, access, and creation times of the current open property set, if supported by the implementation (not all implementations support all these time values). Unsupported time stamps are always reported as zero, enabling the caller to test for support. A call to <a href="https://msdn.microsoft.com/46985c49-cb9b-4f67-8dff-e6fad9e188da">IPropertyStorage::Stat</a> supplies (among other data) time-stamp information.

Notice that this functionality is provided as an 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> method on a property-storage object that is already open, in contrast to being provided as a method in 
<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>. Normally, when the 
<b>SetTimes</b> method is not explicitly called, the access and modification times are updated as a side effect of reading and writing the property set. When 
 <b>SetTimes</b>is used, the latest specified times supersede either default times or time values specified in previous calls to 
<b>SetTimes</b>.




## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/46985c49-cb9b-4f67-8dff-e6fad9e188da">IPropertyStorage::Stat</a>
 

 

