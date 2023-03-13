---
UID: NF:bthledef.IsBthLEUuidMatch
title: IsBthLEUuidMatch
description: Determines whether two UUIDs match each other.
ms.date: 10/20/2022
tech.root: bltooth
req.construct-type: function
req.header: bthledef.h
req.include-header: 
req.target-type: Windows
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
req.lib: BluetoothAPIs.lib
req.dll: BluetoothAPIs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - IsBthLEUuidMatch
 - bthledef/IsBthLEUuidMatch
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - bthledef.h
api_name:
 - IsBthLEUuidMatch
helpviewer_keywords:
 - IsBthLEUuidMatch
---

## -description

Determines whether two UUIDs match each other. If both are short UUIDs, or if both are long UUIDs, then they are compared directly. Otherwise, the short UUID will be converted to a long UUID using the Bluetooth BASE UUID, and then compared against the long one.

## -parameters

### -param uuid1

Type: \_In\_ **[BTH_LE_UUID](/windows/win32/api/bthledef/ns-bthledef-bth_le_uuid)**

Left comparand.

### -param uuid2

Type: \_In\_ **[BTH_LE_UUID](/windows/win32/api/bthledef/ns-bthledef-bth_le_uuid)**

Right comparand.

## -returns

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

**TRUE** if the values are equal, **FALSE** otherwise.

## -remarks

## -see-also
