---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0004
title: DataCollectorSetStatus (pla.h)
description: Defines the running status of the data collector set.
helpviewer_keywords: ["DataCollectorSetStatus","DataCollectorSetStatus enumeration [PLA]","base.datacollectorsetstatus","pla.datacollectorsetstatus","pla/DataCollectorSetStatus","pla/plaCompiling","pla/plaPending","pla/plaRunning","pla/plaStopped","pla/plaUndefined","plaCompiling","plaPending","plaRunning","plaStopped","plaUndefined"]
old-location: pla\datacollectorsetstatus.htm
tech.root: PLA
ms.assetid: 7cccb588-c530-46dc-99e8-84e763cb0a8b
ms.date: 12/05/2018
ms.keywords: DataCollectorSetStatus, DataCollectorSetStatus enumeration [PLA], base.datacollectorsetstatus, pla.datacollectorsetstatus, pla/DataCollectorSetStatus, pla/plaCompiling, pla/plaPending, pla/plaRunning, pla/plaStopped, pla/plaUndefined, plaCompiling, plaPending, plaRunning, plaStopped, plaUndefined
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DataCollectorSetStatus
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_pla_0001_0043_0004
 - pla/__MIDL___MIDL_itf_pla_0001_0043_0004
 - DataCollectorSetStatus
 - pla/DataCollectorSetStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pla.h
api_name:
 - DataCollectorSetStatus
---

# DataCollectorSetStatus enumeration


## -description

Defines the running status of the data collector set.

## -enum-fields

### -field plaStopped:0

The data collector set is not running.

### -field plaRunning:1

The data collector set is running.

### -field plaCompiling:2

The data collector set is performing data management. A running data collector set will transition from <b>plaRunning</b> to <b>plaCompiling</b> if the data manager is enabled.

### -field plaPending:3

The data collector has been set to run, but the service has not started it yet.  Only computers that run operating systems prior to Windows Vista report this status.

### -field plaUndefined:4

Cannot determine the status but no error has occurred. Typically, this status is set for autologgers.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_status">IDataCollectorSet::Status</a>
