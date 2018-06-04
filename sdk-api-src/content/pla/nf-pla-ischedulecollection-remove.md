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

# IScheduleCollection::Remove


## -description


Removes a schedule from the collection.


## -parameters




### -param vSchedule [in]

The zero-based index of the schedule to remove from the collection. The variant type can be VT_I4, VT_UI4, or VT_DISPATCH.


## -returns



Returns S_OK if successful.




## -remarks



If the variant type is VT_DISPATCH, pass the <b>IDispatch</b> interface of the <a href="https://msdn.microsoft.com/b02043c6-5010-45a1-a4a4-ce30cbf0dba0">ISchedule</a> interface to be removed.




## -see-also




<a href="https://msdn.microsoft.com/40b4a77c-5ab4-4443-801c-2e425b6ca1bc">IScheduleCollection</a>



<a href="https://msdn.microsoft.com/92586c08-2f37-4462-b7cb-af58b6cfcecf">IScheduleCollection::Add</a>



<a href="https://msdn.microsoft.com/e9a3afb8-0049-425b-a231-bbb5b56eced7">IScheduleCollection::Clear</a>
 

 

