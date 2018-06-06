---
UID: NS:bthdef._BTH_HCI_EVENT_INFO
title: "_BTH_HCI_EVENT_INFO"
author: windows-sdk-content
description: Used in connection with obtaining WM_DEVICECHANGE messages for Bluetooth.
old-location: bluetooth\bth_hci_event_info.htm
old-project: Bluetooth
ms.assetid: 9cb5eada-2fce-4568-9d2c-530cd39a2e4c
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PBTH_HCI_EVENT_INFO, *PBTH_HCI_EVENT_INFO structure [Bluetooth], BTH_HCI_EVENT_INFO, BTH_HCI_EVENT_INFO structure [Bluetooth], _BTH_HCI_EVENT_INFO, bluetooth.bth_hci_event_info, bthdef/*PBTH_HCI_EVENT_INFO, bthdef/BTH_HCI_EVENT_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: BTH_HCI_EVENT_INFO, *PBTH_HCI_EVENT_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bthdef.h
api_name:
 - BTH_HCI_EVENT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BTH_HCI_EVENT_INFO structure


## -description


The <b>BTH_HCI_EVENT_INFO</b> structure is used in connection with obtaining WM_DEVICECHANGE messages for Bluetooth.


## -struct-fields




### -field bthAddress

Address of the remote device, in the form of a <a href="https://msdn.microsoft.com/81dd4925-7f0a-468f-b706-244ce99e91df">BTH_ADDR</a> structure.


### -field connectionType

Type of connection. Valid values are <b>HCI_CONNECTION_TYPE_ACL</b> or <b>HCI_CONNECTION_TYPE_SCO</b>.


### -field connected

Status of the connection. If nonzero, the connection has been established. If zero, the connection has been terminated.


## -see-also




<a href="https://msdn.microsoft.com/81dd4925-7f0a-468f-b706-244ce99e91df">BTH_ADDR</a>



<a href="https://msdn.microsoft.com/ca28c9cd-a271-48fa-901c-e99e063854d5">Bluetooth and WM_DEVICECHANGE
				Messages</a>
 

 

