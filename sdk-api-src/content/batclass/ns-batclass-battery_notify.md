---
UID: NS:batclass.__unnamed_struct_1
title: BATTERY_NOTIFY
author: windows-sdk-content
description: A battery miniclass driver receives a BATTERY_NOTIFY structure when its BatteryMiniSetStatusNotify routine is called.
old-location: battery\battery_notify.htm
tech.root: battery
ms.assetid: 5bf89418-1d18-460b-b1d1-db6fbb390bc8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PBATTERY_NOTIFY, BATTERY_NOTIFY, BATTERY_NOTIFY structure [Battery Devices], PBATTERY_NOTIFY, PBATTERY_NOTIFY structure pointer [Battery Devices], bat-struct_cd1e6dc5-678c-4529-b852-2832ce2e791b.xml, batclass/BATTERY_NOTIFY, batclass/PBATTERY_NOTIFY, battery.battery_notify"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: batclass.h
req.include-header: Batclass.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - batclass.h
api_name:
 - BATTERY_NOTIFY
product: Windows
targetos: Windows
req.typenames: BATTERY_NOTIFY, *PBATTERY_NOTIFY
req.redist: 
---

# BATTERY_NOTIFY structure


## -description


A battery miniclass driver receives a BATTERY_NOTIFY structure when its <a href="https://msdn.microsoft.com/en-us/library/Ff536277(v=VS.85).aspx">BatteryMiniSetStatusNotify</a> routine is called.


## -struct-fields




### -field PowerState

Contains one or more of the following flags to specify a battery power state: BATTERY_POWER_ON_LINE, BATTERY_DISCHARGING, BATTERY_CHARGING, BATTERY_CRITICAL.


### -field LowCapacity

Specifies a ULONG value indicating the battery capacity below which the class driver requires notification.


### -field HighCapacity

Specifies a ULONG value indicating the battery capacity above which the class driver requires notification.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff536277(v=VS.85).aspx">BatteryMiniSetStatusNotify</a>
 

 

