---
UID: NC:mmiscapi.DRIVERPROC
title: DRIVERPROC (mmiscapi.h)
author: windows-sdk-content
description: Processes driver messages for the installable driver. DriverProc is a driver-supplied function.
old-location: multimedia\driverproc.htm
tech.root: Multimedia
ms.assetid: d9a5535f-6b80-40cc-a20b-b7a342414d7f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DRIVERPROC, DRIVERPROC callback function [Windows Multimedia], DRV_CLOSE, DRV_CONFIGURE, DRV_DISABLE, DRV_ENABLE, DRV_FREE, DRV_INSTALL, DRV_LOAD, DRV_OPEN, DRV_POWER, DRV_QUERYCONFIGURE, DRV_REMOVE, DriverProc callback, _win32_DriverProc, mmsystem/DRIVERPROC, multimedia.driverproc
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mmsystem.h
api_name:
 - DRIVERPROC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DRIVERPROC callback function


## -description



Processes driver messages for the installable driver. <b>DriverProc</b> is a driver-supplied function.




## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4


### -param Arg5








#### - dwDriverId

Identifier of the installable driver.


#### - hdrvr

Handle of the installable driver instance. Each instance of the installable driver has a unique handle.


#### - lParam1

32-bit message-specific value.


#### - lParam2

32-bit message-specific value.


#### - msg

Driver message value. It can be a custom value or one of these standard values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DRV_CLOSE"></a><a id="drv_close"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/98d7fe47-5194-4912-a9d6-3af3d1fa4e60">DRV_CLOSE</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that it should decrement its usage count and unload the driver if the count is zero.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_CONFIGURE"></a><a id="drv_configure"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/0d99fad7-ce79-4574-9fd8-262f7e758866">DRV_CONFIGURE</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that it should display a configuration dialog box. This message is sent only if the driver returns a nonzero value when processing the <a href="https://msdn.microsoft.com/fb2e36a7-8d6b-4b08-b2d7-e128ca7082dc">DRV_QUERYCONFIGURE</a> message.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_DISABLE"></a><a id="drv_disable"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/83e99397-6f0e-4174-9f96-e10c1f17ef0b">DRV_DISABLE</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that its allocated memory is about to be freed.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_ENABLE"></a><a id="drv_enable"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/8aa36f3d-b36c-4460-859c-108a7a450ae5">DRV_ENABLE</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that it has been loaded or reloaded or that Windows has been enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_FREE"></a><a id="drv_free"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67">DRV_FREE</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that it will be discarded.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_INSTALL"></a><a id="drv_install"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/8ee7b30b-600b-49f3-93a7-8faa7b87cfd8">DRV_INSTALL</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that it has been successfully installed.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_LOAD"></a><a id="drv_load"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/f3642d91-cea8-499d-8d2e-bf01a59a7d72">DRV_LOAD</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that it has been successfully loaded.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_OPEN"></a><a id="drv_open"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9">DRV_OPEN</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that it is about to be opened.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_POWER"></a><a id="drv_power"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/b3bbd16a-5b90-4127-a1dd-f2ddfd918f0a">DRV_POWER</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that the device's power source is about to be turned on or off.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_QUERYCONFIGURE"></a><a id="drv_queryconfigure"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/fb2e36a7-8d6b-4b08-b2d7-e128ca7082dc">DRV_QUERYCONFIGURE</a></b></dt>
</dl>
</td>
<td width="60%">
Directs the driver to specify whether it supports the <a href="https://msdn.microsoft.com/0d99fad7-ce79-4574-9fd8-262f7e758866">DRV_CONFIGURE</a> message.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_REMOVE"></a><a id="drv_remove"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/e4f6ce7c-29e5-4256-b08a-13571256207c">DRV_REMOVE</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies the driver that it is about to be removed from the system.

</td>
</tr>
</table>
 


## -returns



Returns nonzero if successful or zero otherwise.




## -remarks



When <i>msg</i> is <a href="https://msdn.microsoft.com/6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9">DRV_OPEN</a>, <i>lParam1</i> is the string following the driver filename from the SYSTEM.INI file and <i>lParam2</i> is the value given as the <i>lParam</i> parameter in a call to the <a href="https://msdn.microsoft.com/882146f7-cd42-45fd-8a5f-7078b64c7ea8">OpenDriver</a> function.

When <i>msg</i> is <a href="https://msdn.microsoft.com/98d7fe47-5194-4912-a9d6-3af3d1fa4e60">DRV_CLOSE</a>, <i>lParam1</i> and <i>lParam2</i> are the same values as the <i>lParam1</i> and <i>lParam2</i> parameters in a call to the <a href="https://msdn.microsoft.com/47d5c666-614d-4836-8e7d-0fe6b53d399f">CloseDriver</a> function.




## -see-also




<a href="https://msdn.microsoft.com/39b00125-b705-4cad-9334-3860a93a4f05">Driver Functions</a>



<a href="https://msdn.microsoft.com/8b628a4d-48fa-4388-9d7c-0c901c45b7f3">Installable Drivers</a>
 

 

