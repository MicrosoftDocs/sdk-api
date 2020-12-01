---
UID: NF:swdevice.SwDeviceGetLifetime
title: SwDeviceGetLifetime function (swdevice.h)
description: Gets the lifetime of a software device.
helpviewer_keywords: ["SWDeviceLifetimeHandle","SWDeviceLifetimeParentPresent","SwDeviceGetLifetime","SwDeviceGetLifetime function","swdevice.swdevicegetlifetime","swdevice/SwDeviceGetLifetime"]
old-location: swdevice\swdevicegetlifetime.htm
tech.root: swdevice
ms.assetid: 62DF53E6-30C5-41D1-867A-9A5D288AADC7
ms.date: 12/05/2018
ms.keywords: SWDeviceLifetimeHandle, SWDeviceLifetimeParentPresent, SwDeviceGetLifetime, SwDeviceGetLifetime function, swdevice.swdevicegetlifetime, swdevice/SwDeviceGetLifetime
req.header: swdevice.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Swdevice.lib; OneCoreUAP.lib on Windows 10
req.dll: Cfgmgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SwDeviceGetLifetime
 - swdevice/SwDeviceGetLifetime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
 - API-MS-Win-devices-swdevice-l1-1-1.dll
api_name:
 - SwDeviceGetLifetime
---

# SwDeviceGetLifetime function


## -description

Gets the lifetime of a software device.

## -parameters

### -param hSwDevice [in]

The <b>HSWDEVICE</b> handle to the software device to retrieve.

### -param pLifetime [in]

A pointer to a variable that receives a <b>SW_DEVICE_LIFETIME</b>-typed value that indicates the current lifetime value for the software device. Here are possible values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SWDeviceLifetimeHandle"></a><a id="swdevicelifetimehandle"></a><a id="SWDEVICELIFETIMEHANDLE"></a><dl>
<dt><b>SWDeviceLifetimeHandle</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the lifetime of the software device is determined by the lifetime of the handle that is associated with the software device.  As long as the handle is open, the software device is enumerated by PnP.

</td>
</tr>
<tr>
<td width="40%"><a id="SWDeviceLifetimeParentPresent"></a><a id="swdevicelifetimeparentpresent"></a><a id="SWDEVICELIFETIMEPARENTPRESENT"></a><dl>
<dt><b>SWDeviceLifetimeParentPresent</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the lifetime of the software device is tied to the lifetime of its parent. 

</td>
</tr>
</table>

## -returns

S_OK is returned if <a href="/windows/desktop/api/swdevice/nf-swdevice-swdevicesetlifetime">SwDeviceSetLifetime</a> successfully retrieved the lifetime.