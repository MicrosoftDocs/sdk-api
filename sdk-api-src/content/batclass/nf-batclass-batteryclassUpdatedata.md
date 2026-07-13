---
UID: NF:batclass.BatteryClassUpdateData
title: BatteryClassUpdateData function (batclass.h)
description: BatteryClassUpdateData notifies notify class driver when battery data is changed. This mechanism is for miniport to report events/status.
helpviewer_keywords: ["BatteryClassUpdateData","BatteryClassUpdateData function [Battery Devices]","bat-rtn_3e9d25d2-bd07-419a-80a5-98fcc08faedd.xml","batclass/BatteryClassUpdateData","battery.BatteryClassUpdateData"]
old-location: battery\BatteryClassUpdateData.htm
tech.root: battery
ms.assetid: b74466e0-d900-49c6-a92e-d10a994fa948
ms.date: 12/05/2018
ms.keywords: BatteryClassUpdateData, BatteryClassUpdateData function [Battery Devices], bat-rtn_3e9d25d2-bd07-419a-80a5-98fcc08faedd.xml, batclass/BatteryClassUpdateData, battery.BatteryClassUpdateData
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
 - BatteryClassUpdateData
 - batclass/BatteryClassUpdateData
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
 - BatteryClassUpdateData
---

# BatteryClassUpdateData function

## -description

<b>BatteryClassUpdateData</b> notifies the battery class driver of changes in battery data.

## -parameters

### -param ClassData [in]

Pointer to a battery class handle previously returned by <a href="/windows/desktop/api/batclass/nf-batclass-batteryclassinitializedevice">BatteryClassInitializeDevice</a>.

### -param MiniportUpdateData [in]

Pointer to <a href="/windows/desktop/api/batclass/ns-batclass-battery_miniport_update_data">BATTERY_MINIPORT_UPDATE_DATA</a> structure.

## -returns

<b>BatteryClassUpdateData</b> returns STATUS_SUCCESS.

## -remarks

This should be called at passive level.

Battery miniclass drivers must call <b>BatteryClassUpdateData</b> whenever any of the following occur:

<ul>
<li>
The battery charge limit changes.

</li>
<li>
The battery's charging status changes, i.e No Power Supply, Inadequate Power Supply or Adequate Power Supply. This is used for barrel charger low wattge indicator.
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/batclass/ns-batclass-battery_miniport_update_data">BATTERY_MINIPORT_UPDATE_DATA</a>