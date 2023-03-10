---
UID: NS:mstask._DAILY
title: DAILY (mstask.h)
description: Defines the interval, in days, at which a task is run.
helpviewer_keywords: ["DAILY","DAILY structure [Task Scheduler]","_msb_daily","mstask/DAILY","taskschd.daily","triggers [Task Scheduler]","structures","DAILY"]
old-location: taskschd\daily.htm
tech.root: taskschd
ms.assetid: 4dbab308-fd1c-4be4-84f6-c12f751ab29e
ms.date: 12/05/2018
ms.keywords: DAILY, DAILY structure [Task Scheduler], _msb_daily, mstask/DAILY, taskschd.daily, triggers [Task Scheduler],structures,DAILY
req.header: mstask.h
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
req.typenames: DAILY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DAILY
 - mstask/_DAILY
 - DAILY
 - mstask/DAILY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstask.h
api_name:
 - DAILY
---

# DAILY structure


## -description

 Defines the interval, in days, at which a task is run.

## -struct-fields

### -field DaysInterval

Specifies the number of days between task runs.

## -remarks

 The 
<a href="/windows/desktop/api/mstask/ns-mstask-trigger_type_union">TRIGGER_TYPE_UNION</a> union uses an instance of this structure as part of the <b>Type</b> member of the 
<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a> structure definition.

## -see-also

<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a>



<a href="/windows/desktop/api/mstask/ns-mstask-trigger_type_union">TRIGGER_TYPE_UNION</a>