---
UID: NF:swdevice.SwDeviceSetLifetime
title: SwDeviceSetLifetime function
author: windows-sdk-content
description: Manages the lifetime of a software device.
old-location: swdevice\swdevicesetlifetime.htm
tech.root: swdevice
ms.assetid: 64CAAA98-9358-4F53-A0AA-EE5984DE9638
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SWDeviceLifetimeHandle, SWDeviceLifetimeParentPresent, SwDeviceSetLifetime, SwDeviceSetLifetime function, swdevice.swdevicesetlifetime, swdevice/SwDeviceSetLifetime
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
 - API-MS-Win-devices-swdevice-l1-1-1.dll
api_name:
 - SwDeviceSetLifetime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SwDeviceSetLifetime function


## -description


Manages the lifetime of a software device. 


## -parameters




### -param hSwDevice [in]

The <b>HSWDEVICE</b> handle to the software device to manage. 


### -param Lifetime [in]

A <b>SW_DEVICE_LIFETIME</b>-typed value that indicates the new lifetime value for the software device. Here are possible values:

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



S_OK is returned if <b>SwDeviceSetLifetime</b> successfully updated the lifetime. 




## -remarks



After a software device is initially created by calling <a href="https://msdn.microsoft.com/8274D7D9-D4AD-412E-A9C0-7D4A08C8A14F">SwDeviceCreate</a>, its default lifetime is set to <b>SwDeviceLifetimeHandle</b>.  When a software device has a lifetime of <b>SwDeviceLifetimeHandle</b>, PnP stops enumerating the device after the device's handle is closed.

You can use <b>SwDeviceSetLifetime</b> to set the lifetime of the software device to <b>SwDeviceLifetimeParentPresent</b>.  The lifetime of the software device is then tied to the lifetime of the closest non-software device parent.  The creator of the software device can then close the handle to the software device and the device will still be enumerated. This can be useful for services that manage software devices but want to idle stop.

A client app can only call <b>SwDeviceSetLifetime</b> after it has received a call to its <a href="https://msdn.microsoft.com/3955FA66-EBE2-4710-A873-C5FC8B7DBE2E">SW_DEVICE_CREATE_CALLBACK</a> callback function that is associated with its call to <a href="https://msdn.microsoft.com/8274D7D9-D4AD-412E-A9C0-7D4A08C8A14F">SwDeviceCreate</a>. 

When a client app calls <a href="https://msdn.microsoft.com/8274D7D9-D4AD-412E-A9C0-7D4A08C8A14F">SwDeviceCreate</a> for a software device that was previously marked for <b>SwDeviceLifetimeParentPresent</b>, <b>SwDeviceCreate</b> succeeds if there are no open software device handles for the device (only one handle can be open for a device).  A client app can then regain control over a persistent software device for the purposes of updating properties and interfaces or changing the lifetime.

If the client app specifies info in <a href="https://msdn.microsoft.com/9519FD17-AB43-4C9E-BE77-9DFAC3263447">SW_DEVICE_CREATE_INFO</a> that is different form a previous enumeration, the device might stop being enumerated and immediately re-enumerated to apply the changes.  The operating system reports only some properties when PnP enumerates the device.

To uninstall a software device with a lifetime of <b>SwDeviceLifetimeParentPresent</b>, we recommend that you change the lifetime back to <b>SwDeviceLifetimeHandle</b> before the device is uninstalled.



