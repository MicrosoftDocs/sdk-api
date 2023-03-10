---
UID: NC:batclass.BCLASS_QUERY_TAG_CALLBACK
title: BCLASS_QUERY_TAG_CALLBACK (batclass.h)
description: BatteryMiniQueryTag returns the current battery tag.
helpviewer_keywords: ["BCLASS_QUERY_TAG_CALLBACK","BCLASS_QUERY_TAG_CALLBACK callback","BatteryMiniQueryTag","BatteryMiniQueryTag callback function [Battery Devices]","bat-mini_67f7c8df-433f-43fa-bca1-206f9e0932bb.xml","batclass/BatteryMiniQueryTag","battery.batteryminiquerytag"]
old-location: battery\batteryminiquerytag.htm
tech.root: battery
ms.assetid: 030b7f5f-8ace-4dfc-8330-97aace86a1eb
ms.date: 12/05/2018
ms.keywords: BCLASS_QUERY_TAG_CALLBACK, BCLASS_QUERY_TAG_CALLBACK callback, BatteryMiniQueryTag, BatteryMiniQueryTag callback function [Battery Devices], bat-mini_67f7c8df-433f-43fa-bca1-206f9e0932bb.xml, batclass/BatteryMiniQueryTag, battery.batteryminiquerytag
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
 - BCLASS_QUERY_TAG_CALLBACK
 - batclass/BCLASS_QUERY_TAG_CALLBACK
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
 - BatteryMiniQueryTag
---

# BCLASS_QUERY_TAG_CALLBACK callback function


## -description

<i>BatteryMiniQueryTag</i> returns the current battery tag.

## -parameters

### -param Context [in]

A pointer to the context area allocated by the miniclass driver for the battery device.

### -param BatteryTag [out]

A pointer to a caller-allocated variable in which the miniclass driver returns the battery tag.

## -returns

<i>BatteryMiniQueryTag</i> returns one of the following:

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
No battery is present. 

</td>
</tr>
</table>

## -remarks

The battery class driver calls <i>BatteryMiniQueryTag</i> to get the value of the current battery tag. If a battery is present, <i>BatteryMiniQueryTag</i> should return the tag in <i>BatteryTag</i> and return STATUS_SUCCESS. 

Each time a battery is inserted, the miniclass driver must increment the value of the tag, regardless of whether this is a new battery or the same battery that was previously present. 

If no battery is present, or if the miniclass driver cannot determine whether a battery is present, it should return STATUS_NO_SUCH_DEVICE and set the value of the tag to BATTERY_TAG_INVALID.

