---
UID: NF:batclass.BatteryClassUnload
title: BatteryClassUnload function
author: windows-sdk-content
description: BatteryClassUnload frees resources for a battery device that is no longer in use.
old-location: battery\batteryclassunload.htm
tech.root: battery
ms.assetid: 6825a798-f7b3-49bc-91b3-69d05c0eef26
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BatteryClassUnload, BatteryClassUnload function [Battery Devices], bat-rtn_d99ad46b-2f22-4e88-9f26-f86fb6b09bee.xml, batclass/BatteryClassUnload, battery.batteryclassunload
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Battc.lib
 - Battc.dll
api_name:
 - BatteryClassUnload
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BatteryClassUnload function


## -description


<b>BatteryClassUnload</b> frees resources for a battery device that is no longer in use.


## -parameters




### -param ClassData [in]

Pointer to a battery class handle previously returned by <a href="https://msdn.microsoft.com/en-us/library/Ff536266(v=VS.85).aspx">BatteryClassInitializeDevice</a>.


## -returns



<b>BatteryClassUnload</b> returns STATUS_SUCCESS.




## -remarks



<b>BatteryClassUnload</b> frees the battery class handle and unloads the battery device. In essence, it undoes the registration and initialization performed by <b>BatteryClassInitializeDevice</b>.

A miniclass driver should call this routine when its battery device is no longer available for use. Typically, the driver might make such a call from its Unload routine or when handling a PnP <a href="https://msdn.microsoft.com/0d733cbd-2da8-48a5-afc6-e1e6b8f507a1">IRP_MN_REMOVE_DEVICE</a> request.



