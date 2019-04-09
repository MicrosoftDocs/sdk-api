---
UID: NF:pla.IScheduleCollection.Remove
title: IScheduleCollection::Remove (pla.h)
author: windows-sdk-content
description: Removes a schedule from the collection.
old-location: pla\ischedulecollection_remove.htm
tech.root: PLA
ms.assetid: bb419f7e-b5fd-47ea-88e5-f86788423edf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IScheduleCollection interface [PLA],Remove method, IScheduleCollection.Remove, IScheduleCollection::Remove, Remove, Remove method [PLA], Remove method [PLA],IScheduleCollection interface, base.ischedulecollection_remove, pla.ischedulecollection_remove, pla/IScheduleCollection::Remove
ms.topic: method
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Pla.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IScheduleCollection.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

