---
UID: NF:pla.IScheduleCollection.Add
title: IScheduleCollection::Add (pla.h)
description: Adds a schedule to the collection.
helpviewer_keywords: ["Add","Add method [PLA]","Add method [PLA]","IScheduleCollection interface","IScheduleCollection interface [PLA]","Add method","IScheduleCollection.Add","IScheduleCollection::Add","base.ischedulecollection_add","pla.ischedulecollection_add","pla/IScheduleCollection::Add"]
old-location: pla\ischedulecollection_add.htm
tech.root: PLA
ms.assetid: 92586c08-2f37-4462-b7cb-af58b6cfcecf
ms.date: 12/05/2018
ms.keywords: Add, Add method [PLA], Add method [PLA],IScheduleCollection interface, IScheduleCollection interface [PLA],Add method, IScheduleCollection.Add, IScheduleCollection::Add, base.ischedulecollection_add, pla.ischedulecollection_add, pla/IScheduleCollection::Add
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IScheduleCollection::Add
 - pla/IScheduleCollection::Add
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IScheduleCollection.Add
---

# IScheduleCollection::Add


## -description

Adds a schedule to the collection.

## -parameters

### -param pSchedule [in]

An <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ischedule">ISchedule</a> interface of the schedule to add to the collection.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-ischedulecollection">IScheduleCollection</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-ischedulecollection-addrange">IScheduleCollection::AddRange</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-ischedulecollection-remove">IScheduleCollection::Remove</a>