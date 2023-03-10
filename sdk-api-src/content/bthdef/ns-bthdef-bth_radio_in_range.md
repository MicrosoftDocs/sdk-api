---
UID: NS:bthdef._BTH_RADIO_IN_RANGE
title: BTH_RADIO_IN_RANGE (bthdef.h)
description: Stores data about Bluetooth devices within communication range.
helpviewer_keywords: ["*PBTH_RADIO_IN_RANGE","*PBTH_RADIO_IN_RANGE structure [Bluetooth]","BTH_RADIO_IN_RANGE","BTH_RADIO_IN_RANGE structure [Bluetooth]","bluetooth.bth_radio_in_range","bthdef/*PBTH_RADIO_IN_RANGE","bthdef/BTH_RADIO_IN_RANGE"]
old-location: bluetooth\bth_radio_in_range.htm
tech.root: bluetooth
ms.assetid: 997c50bb-1313-409a-9a24-9225a6cf91d9
ms.date: 12/05/2018
ms.keywords: '*PBTH_RADIO_IN_RANGE, *PBTH_RADIO_IN_RANGE structure [Bluetooth], BTH_RADIO_IN_RANGE, BTH_RADIO_IN_RANGE structure [Bluetooth], bluetooth.bth_radio_in_range, bthdef/*PBTH_RADIO_IN_RANGE, bthdef/BTH_RADIO_IN_RANGE'
req.header: bthdef.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BTH_RADIO_IN_RANGE, *PBTH_RADIO_IN_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BTH_RADIO_IN_RANGE
 - bthdef/_BTH_RADIO_IN_RANGE
 - PBTH_RADIO_IN_RANGE
 - bthdef/PBTH_RADIO_IN_RANGE
 - BTH_RADIO_IN_RANGE
 - bthdef/BTH_RADIO_IN_RANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bthdef.h
api_name:
 - BTH_RADIO_IN_RANGE
---

# BTH_RADIO_IN_RANGE structure


## -description

The <b>BTH_RADIO_IN_RANGE</b> structure stores data about Bluetooth devices within communication range.

## -struct-fields

### -field deviceInfo

Current set of attributes associated with the remote device, in the form of a <a href="/windows/desktop/api/bthdef/ns-bthdef-bth_device_info">BTH_DEVICE_INFO</a> structure.

### -field previousDeviceFlags

Previous flags for the <b>flags</b> member of the <a href="/windows/desktop/api/bthdef/ns-bthdef-bth_device_info">BTH_DEVICE_INFO</a> structure pointed to by the <b>deviceInfo</b> member. Used to determine which attributes associated with the remote device have changed.

## -see-also

<a href="/windows/desktop/api/bthdef/ns-bthdef-bth_device_info">BTH_DEVICE_INFO</a>



<a href="/windows/desktop/Bluetooth/bluetooth-and-wm-devicechange-messages">Bluetooth and WM_DEVICECHANGE
				Messages</a>