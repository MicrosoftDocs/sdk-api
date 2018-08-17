---
UID: NS:bthdef._BTH_RADIO_IN_RANGE
title: "_BTH_RADIO_IN_RANGE"
author: windows-sdk-content
description: Stores data about Bluetooth devices within communication range.
old-location: bluetooth\bth_radio_in_range.htm
old-project: bluetooth
ms.assetid: 997c50bb-1313-409a-9a24-9225a6cf91d9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PBTH_RADIO_IN_RANGE, *PBTH_RADIO_IN_RANGE structure [Bluetooth], BTH_RADIO_IN_RANGE, BTH_RADIO_IN_RANGE structure [Bluetooth], _BTH_RADIO_IN_RANGE, bluetooth.bth_radio_in_range, bthdef/*PBTH_RADIO_IN_RANGE, bthdef/BTH_RADIO_IN_RANGE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: bthdef.h
req.include-header: 
req.redist: 
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
req.typenames: BTH_RADIO_IN_RANGE, *PBTH_RADIO_IN_RANGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bthdef.h
api_name:
 - BTH_RADIO_IN_RANGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BTH_RADIO_IN_RANGE structure


## -description


The <b>BTH_RADIO_IN_RANGE</b> structure stores data about Bluetooth devices within communication range.


## -struct-fields




### -field deviceInfo

Current set of attributes associated with the remote device, in the form of a <a href="https://msdn.microsoft.com/en-us/library/Aa362934(v=VS.85).aspx">BTH_DEVICE_INFO</a> structure.


### -field previousDeviceFlags

Previous flags for the <b>flags</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Aa362934(v=VS.85).aspx">BTH_DEVICE_INFO</a> structure pointed to by the <b>deviceInfo</b> member. Used to determine which attributes associated with the remote device have changed.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362934(v=VS.85).aspx">BTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/7dab37a6-63ac-4377-9884-61dd19972433">Bluetooth and WM_DEVICECHANGE
				Messages</a>
 

 

