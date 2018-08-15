---
UID: NC:batclass.BCLASS_SET_STATUS_NOTIFY_CALLBACK
title: BCLASS_SET_STATUS_NOTIFY_CALLBACK
author: windows-sdk-content
description: BatteryMiniSetStatusNotify sets the battery capacity and power state levels at which the class driver requires notification.
old-location: battery\batteryminisetstatusnotify.htm
old-project: battery
ms.assetid: ec463202-4c08-475a-b612-73413f1376fc
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: BCLASS_SET_STATUS_NOTIFY_CALLBACK, BCLASS_SET_STATUS_NOTIFY_CALLBACK callback, BatteryMiniSetStatusNotify, BatteryMiniSetStatusNotify callback function [Battery Devices], bat-mini_a7e948a0-2fe9-4727-88e1-9eb27272789d.xml, batclass/BatteryMiniSetStatusNotify, battery.batteryminisetstatusnotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: batclass.h
req.include-header: Batclass.h
req.redist: 
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Batclass.h
api_name:
 - BatteryMiniSetStatusNotify
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL
---

# BCLASS_SET_STATUS_NOTIFY_CALLBACK callback function


## -description


<i>BatteryMiniSetStatusNotify</i> sets the battery capacity and power state levels at which the class driver requires notification.


## -parameters




### -param Context [in]

A pointer to the context area allocated by the miniclass driver for the battery device.


### -param BatteryTag [in]

A battery tag value previously returned by <i>BatteryMiniQueryTag</i>.


### -param BatteryNotify [in]

A pointer to a <a href="https://msdn.microsoft.com/5bf89418-1d18-460b-b1d1-db6fbb390bc8">BATTERY_NOTIFY</a> structure. 


## -returns



<i>BatteryMiniSetStatusNotify</i> returns one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
A battery is currently installed. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
No battery is present or the given battery tag is invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The miniclass driver cannot distinguish the target condition.

</td>
</tr>
</table>
 




## -remarks



The battery class driver calls a miniclass driver's <i>BatteryMiniSetStatusNotify</i> routine to set criteria for an acceptable range of battery conditions. When the battery's capacity or power state deviates from these criteria, the miniclass driver must call <a href="https://msdn.microsoft.com/b74466e0-d900-49c6-a92e-d10a994fa948">BatteryClassStatusNotify</a> to notify the class driver.

In the <b>PowerState</b> member of the <a href="https://msdn.microsoft.com/5bf89418-1d18-460b-b1d1-db6fbb390bc8">BATTERY_NOTIFY</a> structure, the class driver specifies one or more battery power states. Any time the battery enters a power state that is not in <b>PowerState</b>, the miniclass driver must notify the class driver.

In the <b>LowCapacity</b> and <b>HighCapacity</b> members of BATTERY_NOTIFY, the class driver specifies a range of capacity. When the capacity falls above or below this range, the miniclass driver must notify the class driver. 

Some batteries might be unable to distinguish the precise capacities requested by the battery class driver. When possible, miniclass drivers for these batteries should attempt to correct for the error so that the user can be informed when the battery approaches a critical state. Otherwise, such drivers should return STATUS_NOT_SUPPORTED.




## -see-also




<a href="https://msdn.microsoft.com/b74466e0-d900-49c6-a92e-d10a994fa948">BatteryClassStatusNotify</a>



<a href="https://msdn.microsoft.com/5120205f-0d55-4391-a560-3089fbe11d82">BatteryMiniDisableStatusNotify</a>
 

 

