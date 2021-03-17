---
UID: NF:batclass.BatteryClassStatusNotify
title: BatteryClassStatusNotify function (batclass.h)
description: BatteryClassStatusNotify notifies the battery class driver of changes in battery status.
helpviewer_keywords: ["BatteryClassStatusNotify","BatteryClassStatusNotify function [Battery Devices]","bat-rtn_3e9d25d2-bd07-419a-80a5-98fcc08faedd.xml","batclass/BatteryClassStatusNotify","battery.batteryclassstatusnotify"]
old-location: battery\batteryclassstatusnotify.htm
tech.root: battery
ms.assetid: b74466e0-d900-49c6-a92e-d10a994fa948
ms.date: 12/05/2018
ms.keywords: BatteryClassStatusNotify, BatteryClassStatusNotify function [Battery Devices], bat-rtn_3e9d25d2-bd07-419a-80a5-98fcc08faedd.xml, batclass/BatteryClassStatusNotify, battery.batteryclassstatusnotify
req.header: batclass.h
req.include-header: Batclass.h
req.target-type: Desktop
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
req.lib: Battc.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BatteryClassStatusNotify
 - batclass/BatteryClassStatusNotify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Battc.lib
 - Battc.dll
api_name:
 - BatteryClassStatusNotify
---

# BatteryClassStatusNotify function


## -description

<b>BatteryClassStatusNotify</b> notifies the battery class driver of changes in battery status.

## -parameters

### -param ClassData [in]

Pointer to a battery class handle previously returned by <a href="/windows/desktop/api/batclass/nf-batclass-batteryclassinitializedevice">BatteryClassInitializeDevice</a>.

## -returns

<b>BatteryClassStatusNotify</b> returns STATUS_SUCCESS.

## -remarks

Battery miniclass drivers must call <b>BatteryClassStatusNotify</b> whenever any of the following occur:

<ul>
<li>
The battery goes online or offline.

</li>
<li>
The battery's capacity becomes critically low.

</li>
<li>
The battery's power state changes; that is, the battery starts or stops charging or discharging.

</li>
<li>
The battery's capacity or power state deviates from the criteria set by a previous call to <a href="/windows/desktop/api/batclass/nc-batclass-bclass_set_status_notify_callback">BatteryMiniSetStatusNotify</a>. 

</li>
</ul>
The battery class driver queues status requests internally. If any such requests are pending when the miniclass driver calls <b>BatteryClassStatusNotify</b>, the class driver immediately calls the miniclass driver's <a href="/windows/desktop/api/batclass/nc-batclass-bclass_query_status_callback">BatteryMiniQueryStatus</a> routine.

## -see-also

<a href="/windows/desktop/api/batclass/nc-batclass-bclass_query_status_callback">BatteryMiniQueryStatus</a>



<a href="/windows/desktop/api/batclass/nc-batclass-bclass_set_status_notify_callback">BatteryMiniSetStatusNotify</a>