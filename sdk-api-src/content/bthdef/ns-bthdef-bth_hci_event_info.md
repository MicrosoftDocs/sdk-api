---
UID: NS:bthdef._BTH_HCI_EVENT_INFO
title: BTH_HCI_EVENT_INFO (bthdef.h)
description: Used in connection with obtaining WM_DEVICECHANGE messages for Bluetooth.
helpviewer_keywords: ["*PBTH_HCI_EVENT_INFO","*PBTH_HCI_EVENT_INFO structure [Bluetooth]","BTH_HCI_EVENT_INFO","BTH_HCI_EVENT_INFO structure [Bluetooth]","bluetooth.bth_hci_event_info","bthdef/*PBTH_HCI_EVENT_INFO","bthdef/BTH_HCI_EVENT_INFO"]
old-location: bluetooth\bth_hci_event_info.htm
tech.root: bluetooth
ms.assetid: 9cb5eada-2fce-4568-9d2c-530cd39a2e4c
ms.date: 12/05/2018
ms.keywords: '*PBTH_HCI_EVENT_INFO, *PBTH_HCI_EVENT_INFO structure [Bluetooth], BTH_HCI_EVENT_INFO, BTH_HCI_EVENT_INFO structure [Bluetooth], bluetooth.bth_hci_event_info, bthdef/*PBTH_HCI_EVENT_INFO, bthdef/BTH_HCI_EVENT_INFO'
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
req.typenames: BTH_HCI_EVENT_INFO, *PBTH_HCI_EVENT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BTH_HCI_EVENT_INFO
 - bthdef/_BTH_HCI_EVENT_INFO
 - PBTH_HCI_EVENT_INFO
 - bthdef/PBTH_HCI_EVENT_INFO
 - BTH_HCI_EVENT_INFO
 - bthdef/BTH_HCI_EVENT_INFO
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
 - BTH_HCI_EVENT_INFO
---

# BTH_HCI_EVENT_INFO structure


## -description

The <b>BTH_HCI_EVENT_INFO</b> structure is used in connection with obtaining WM_DEVICECHANGE messages for Bluetooth.

## -struct-fields

### -field bthAddress

Address of the remote device, in the form of a <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothauthenticatemultipledevices">BTH_ADDR</a> structure.

### -field connectionType

Type of connection. Valid values are <b>HCI_CONNECTION_TYPE_ACL</b> or <b>HCI_CONNECTION_TYPE_SCO</b>.

### -field connected

Status of the connection. If nonzero, the connection has been established. If zero, the connection has been terminated.

## -see-also

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothauthenticatemultipledevices">BTH_ADDR</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothenablediscovery">Bluetooth and WM_DEVICECHANGE
				Messages</a>