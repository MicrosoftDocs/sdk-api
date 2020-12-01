---
UID: NF:pla.IScheduleCollection.Remove
title: IScheduleCollection::Remove (pla.h)
description: Removes a schedule from the collection.
helpviewer_keywords: ["IScheduleCollection interface [PLA]","Remove method","IScheduleCollection.Remove","IScheduleCollection::Remove","Remove","Remove method [PLA]","Remove method [PLA]","IScheduleCollection interface","base.ischedulecollection_remove","pla.ischedulecollection_remove","pla/IScheduleCollection::Remove"]
old-location: pla\ischedulecollection_remove.htm
tech.root: PLA
ms.assetid: bb419f7e-b5fd-47ea-88e5-f86788423edf
ms.date: 12/05/2018
ms.keywords: IScheduleCollection interface [PLA],Remove method, IScheduleCollection.Remove, IScheduleCollection::Remove, Remove, Remove method [PLA], Remove method [PLA],IScheduleCollection interface, base.ischedulecollection_remove, pla.ischedulecollection_remove, pla/IScheduleCollection::Remove
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
 - IScheduleCollection::Remove
 - pla/IScheduleCollection::Remove
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
 - IScheduleCollection.Remove
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

If the variant type is VT_DISPATCH, pass the <b>IDispatch</b> interface of the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ischedule">ISchedule</a> interface to be removed.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-ischedulecollection">IScheduleCollection</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-ischedulecollection-add">IScheduleCollection::Add</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-ischedulecollection-clear">IScheduleCollection::Clear</a>