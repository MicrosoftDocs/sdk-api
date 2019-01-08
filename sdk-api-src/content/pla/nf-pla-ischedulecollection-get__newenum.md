---
UID: NF:pla.IScheduleCollection.get__NewEnum
title: IScheduleCollection::get__NewEnum
author: windows-sdk-content
description: Retrieves an interface to the enumeration.
old-location: pla\ischedulecollection__newenum.htm
tech.root: PLA
ms.assetid: 4aae67ae-8b9d-4baa-b617-b6e44b7e7edf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IScheduleCollection interface [PLA],_NewEnum property, IScheduleCollection._NewEnum, IScheduleCollection.get__NewEnum, IScheduleCollection::_NewEnum, IScheduleCollection::get__NewEnum, _NewEnum property [PLA], _NewEnum property [PLA],IScheduleCollection interface, get__NewEnum, pla.ischedulecollection__newenum, pla/IScheduleCollection::_NewEnum, pla/IScheduleCollection::get__NewEnum
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
 - IScheduleCollection._NewEnum
 - IScheduleCollection.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IScheduleCollection::get__NewEnum


## -description


Retrieves an interface to the enumeration.

This property is read-only.


## -parameters


## -remarks



 C++ programmers use this property.

The enumeration is a snapshot of the collection at the time of the call.

The items of the enumeration are variants whose type is VT_UNKNOWN. To query for the <a href="https://msdn.microsoft.com/b02043c6-5010-45a1-a4a4-ce30cbf0dba0">ISchedule</a> interface, use the <b>punkVal</b> member of the variant.




## -see-also




<a href="https://msdn.microsoft.com/40b4a77c-5ab4-4443-801c-2e425b6ca1bc">IScheduleCollection</a>
 

 

