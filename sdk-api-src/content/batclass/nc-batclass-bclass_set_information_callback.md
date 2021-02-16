---
UID: NC:batclass.BCLASS_SET_INFORMATION_CALLBACK
title: BCLASS_SET_INFORMATION_CALLBACK (batclass.h)
description: BatteryMiniSetInformation requests that a battery enter the charging or discharging state, or sets a critical bias value for the battery.
helpviewer_keywords: ["BCLASS_SET_INFORMATION_CALLBACK","BCLASS_SET_INFORMATION_CALLBACK callback","BatteryMiniSetInformation","BatteryMiniSetInformation callback function [Battery Devices]","bat-mini_abc151e1-9d35-4b39-b1e8-576503335d3b.xml","batclass/BatteryMiniSetInformation","battery.batteryminisetinformation"]
old-location: battery\batteryminisetinformation.htm
tech.root: battery
ms.assetid: ebfcabb7-7447-486d-b980-7cb5456332f4
ms.date: 12/05/2018
ms.keywords: BCLASS_SET_INFORMATION_CALLBACK, BCLASS_SET_INFORMATION_CALLBACK callback, BatteryMiniSetInformation, BatteryMiniSetInformation callback function [Battery Devices], bat-mini_abc151e1-9d35-4b39-b1e8-576503335d3b.xml, batclass/BatteryMiniSetInformation, battery.batteryminisetinformation
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
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCLASS_SET_INFORMATION_CALLBACK
 - batclass/BCLASS_SET_INFORMATION_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Batclass.h
api_name:
 - BatteryMiniSetInformation
---

# BCLASS_SET_INFORMATION_CALLBACK callback function


## -description

<i>BatteryMiniSetInformation</i> requests that a battery enter the charging or discharging state, or sets a critical bias value for the battery.

## -parameters

### -param Context [in]

A pointer to the context area allocated by the miniclass driver for the battery device.

### -param BatteryTag [in]

A battery tag value previously returned by <i>BatteryMiniQueryTag</i>.

### -param Level [in]

One of the following values: <b>BatteryCriticalBias</b>, <b>BatteryCharge</b>, or <b>BatteryDischarge.</b>

### -param Buffer [in]

The critical bias adjustment in milliwatts if <i>Level</i> is <b>BatteryCriticalBias</b>. Not used for other values of <i>Level</i>.

## -returns

<i>BatteryMiniSetInformation</i> returns one of the following: 

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
The operation succeeded. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
No battery is present. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The specified battery does not support the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_UNSUCCESSFUL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
</table>

## -remarks

The battery class driver calls <i>BatteryMiniSetInformation</i> to request that a battery start to charge or discharge. It can also call this routine to set a critical bias value. 

With a smart battery charger/selector, the class driver specifies <b>BatteryCharge</b> to select a battery to charge, possibly discontinuing the charging of another battery.

The class driver specifies <b>BatteryDischarge</b> to indicate which battery should power the system.

The critical bias adjustment is analogous to the reserve capacity of the gas tank in an automobile. It represents the remaining charge when the battery capacity is reported as zero. Although the class driver does not change the critical bias value in normal use, this field is provided in the interface as a maintenance feature. Not all batteries can maintain a critical bias setting. Miniclass drivers for such batteries should return STATUS_NOT_SUPPORTED.

