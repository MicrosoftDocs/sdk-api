---
UID: NC:mmiscapi.DRIVERPROC
title: DRIVERPROC (mmiscapi.h)
description: Processes driver messages for the installable driver. DriverProc is a driver-supplied function.
helpviewer_keywords: ["DRIVERPROC","DRIVERPROC callback function [Windows Multimedia]","DRV_CLOSE","DRV_CONFIGURE","DRV_DISABLE","DRV_ENABLE","DRV_FREE","DRV_INSTALL","DRV_LOAD","DRV_OPEN","DRV_POWER","DRV_QUERYCONFIGURE","DRV_REMOVE","DriverProc callback","_win32_DriverProc","mmsystem/DRIVERPROC","multimedia.driverproc"]
old-location: multimedia\driverproc.htm
tech.root: Multimedia
ms.assetid: d9a5535f-6b80-40cc-a20b-b7a342414d7f
ms.date: 12/05/2018
ms.keywords: DRIVERPROC, DRIVERPROC callback function [Windows Multimedia], DRV_CLOSE, DRV_CONFIGURE, DRV_DISABLE, DRV_ENABLE, DRV_FREE, DRV_INSTALL, DRV_LOAD, DRV_OPEN, DRV_POWER, DRV_QUERYCONFIGURE, DRV_REMOVE, DriverProc callback, _win32_DriverProc, mmsystem/DRIVERPROC, multimedia.driverproc
req.header: mmiscapi.h
req.include-header: Mmiscapi.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DRIVERPROC
 - mmiscapi/DRIVERPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mmsystem.h
api_name:
 - DRIVERPROC
---

# DRIVERPROC callback function


## -description

Processes driver messages for the installable driver. <b>DriverProc</b> is a driver-supplied function.

## -parameters

### -param unnamedParam1

Identifier of the installable driver.

### -param unnamedParam2

Handle of the installable driver instance. Each instance of the installable driver has a unique handle.

### -param unnamedParam3

Driver message value. It can be a custom value or one of these standard values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DRV_CLOSE"></a><a id="drv_close"></a><dl>
<dt><b><a href="/windows/desktop/Multimedia/drv-close">DRV_CLOSE</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that it should decrement its usage count and unload the driver if the count is zero.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_CONFIGURE"></a><a id="drv_configure"></a><dl>
<dt><b><a href="/windows/desktop/Multimedia/drv-configure">DRV_CONFIGURE</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that it should display a configuration dialog box. This message is sent only if the driver returns a nonzero value when processing the <a href="/windows/desktop/Multimedia/drv-queryconfigure">DRV_QUERYCONFIGURE</a> message.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_DISABLE"></a><a id="drv_disable"></a><dl>
<dt><b><a href="/windows/desktop/Multimedia/drv-disable">DRV_DISABLE</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that its allocated memory is about to be freed.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_ENABLE"></a><a id="drv_enable"></a><dl>
<dt><b><a href="/windows/desktop/Multimedia/drv-enable">DRV_ENABLE</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that it has been loaded or reloaded or that Windows has been enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_FREE"></a><a id="drv_free"></a><dl>
<dt><b><a href="/windows/desktop/Multimedia/drv-free">DRV_FREE</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that it will be discarded.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_INSTALL"></a><a id="drv_install"></a><dl>
<dt><b><a href="/windows/desktop/Multimedia/drv-install">DRV_INSTALL</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that it has been successfully installed.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_LOAD"></a><a id="drv_load"></a><dl>
<dt><b><a href="/windows/desktop/Multimedia/drv-load">DRV_LOAD</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that it has been successfully loaded.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_OPEN"></a><a id="drv_open"></a><dl>
<dt><b><a href="/windows/desktop/Multimedia/drv-open">DRV_OPEN</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that it is about to be opened.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_POWER"></a><a id="drv_power"></a><dl>
<dt><b><a href="/windows/desktop/Multimedia/drv-power">DRV_POWER</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that the device's power source is about to be turned on or off.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_QUERYCONFIGURE"></a><a id="drv_queryconfigure"></a><dl>
<dt><b><a href="/windows/desktop/Multimedia/drv-queryconfigure">DRV_QUERYCONFIGURE</a></b></dt>
</dl>
</td>
<td width="60%">
Directs the driver to specify whether it supports the <a href="/windows/desktop/Multimedia/drv-configure">DRV_CONFIGURE</a> message.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_REMOVE"></a><a id="drv_remove"></a><dl>
<dt><b><a href="/windows/desktop/Multimedia/drv-remove">DRV_REMOVE</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that it is about to be removed from the system.

</td>
</tr>
</table>

### -param unnamedParam4

32-bit message-specific value.

### -param unnamedParam5

32-bit message-specific value.

## -returns

Returns nonzero if successful or zero otherwise.

## -remarks

When <i>msg</i> is <a href="/windows/desktop/Multimedia/drv-open">DRV_OPEN</a>, <i>lParam1</i> is the string following the driver filename from the SYSTEM.INI file and <i>lParam2</i> is the value given as the <i>lParam</i> parameter in a call to the <a href="/previous-versions/dd743639(v=vs.85)">OpenDriver</a> function.

When <i>msg</i> is <a href="/windows/desktop/Multimedia/drv-close">DRV_CLOSE</a>, <i>lParam1</i> and <i>lParam2</i> are the same values as the <i>lParam1</i> and <i>lParam2</i> parameters in a call to the <a href="/previous-versions/dd797785(v=vs.85)">CloseDriver</a> function.

## -see-also

<a href="/windows/desktop/Multimedia/driver-functions">Driver Functions</a>



<a href="/windows/desktop/Multimedia/installable-drivers">Installable Drivers</a>