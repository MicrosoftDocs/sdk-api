---
UID: NS:eventsys.__MIDL___MIDL_itf_eventsys_0000_0009_0001
title: COMEVENTSYSCHANGEINFO (eventsys.h)
description: Represents a system event structure, which contains the partition and application ID from which an event originated.
helpviewer_keywords: ["COMEVENTSYSCHANGEINFO","COMEVENTSYSCHANGEINFO structure [COM+]","_cos_COMEVENTSYSCHANGEINFO","cos.comeventsyschangeinfo","eventsys/COMEVENTSYSCHANGEINFO"]
old-location: cos\comeventsyschangeinfo.htm
tech.root: cos
ms.assetid: 6c9f143e-bdd4-48be-a635-a382c8c770c1
ms.date: 12/05/2018
ms.keywords: COMEVENTSYSCHANGEINFO, COMEVENTSYSCHANGEINFO structure [COM+], _cos_COMEVENTSYSCHANGEINFO, cos.comeventsyschangeinfo, eventsys/COMEVENTSYSCHANGEINFO
req.header: eventsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: COMEVENTSYSCHANGEINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_eventsys_0000_0009_0001
 - eventsys/__MIDL___MIDL_itf_eventsys_0000_0009_0001
 - COMEVENTSYSCHANGEINFO
 - eventsys/COMEVENTSYSCHANGEINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - EventSys.h
api_name:
 - COMEVENTSYSCHANGEINFO
---

# COMEVENTSYSCHANGEINFO structure


## -description

Represents a system event structure, which contains the partition and application ID from which an event originated.

## -struct-fields

### -field cbSize

The size of this structure.

### -field changeType

The type of change that has been made to the subscription. For a list of values, see <a href="/windows/desktop/api/eventsys/ne-eventsys-eoc_changetype">EOC_ChangeType</a>.

### -field objectId

The EventClass ID or subscription ID from which the change impacts.

### -field partitionId

The EventClass partition ID or the subscriber partition ID affected.

### -field applicationId

The EventClass application ID or subscriber application ID affected.

### -field reserved

This member is reserved.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventobjectchange2">IEventObjectChange2</a>