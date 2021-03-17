---
UID: NF:bluetoothapis.BluetoothIsVersionAvailable
title: BluetoothIsVersionAvailable function (bluetoothapis.h)
description: BluetoothIsVersionAvailable function indicates if the installed Bluetooth binary set supports the requested version.
helpviewer_keywords: ["BluetoothIsVersionAvailable","BluetoothIsVersionAvailable function [Bluetooth]","bluetooth.bluetoothisversionavailable","bluetoothapis/BluetoothIsVersionAvailable"]
old-location: bluetooth\bluetoothisversionavailable.htm
tech.root: bluetooth
ms.assetid: 735a4c3f-1977-4600-afb2-272de3f4e7ba
ms.date: 12/05/2018
ms.keywords: BluetoothIsVersionAvailable, BluetoothIsVersionAvailable function [Bluetooth], bluetooth.bluetoothisversionavailable, bluetoothapis/BluetoothIsVersionAvailable
req.header: bluetoothapis.h
req.include-header: Bthsdpdef.h, BluetoothAPIs.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bthprops.lib
req.dll: Bthprops.cpl
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BluetoothIsVersionAvailable
 - bluetoothapis/BluetoothIsVersionAvailable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bthprops.cpl
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothIsVersionAvailable
---

# BluetoothIsVersionAvailable function


## -description

The <b>BluetoothIsVersionAvailable</b> function indicates if the installed Bluetooth binary set supports      the requested version.

## -parameters

### -param MajorVersion [in]

The major version number.

### -param MinorVersion [in]

The minor version number.

## -returns

<b>TRUE</b> if the installed bluetooth binaries support the specified <i>MajorVersion</i> and <i>MinorVersion</i>; otherwise, <b>FALSE</b>.

## -remarks

This functionality is only exported in Bluetooth for Windows version 2.1 and later.

