---
UID: NF:swdevice.SwDeviceClose
title: SwDeviceClose function (swdevice.h)
description: Closes the software device handle. When the handle is closed, if the lifetime of the SwDevice is SWDeviceLifetimeHandle, PnP will initiate the process of "unplugging" the device. The device will no longer be reported as a child of its parent device.
helpviewer_keywords: ["SwDeviceClose","SwDeviceClose function","swdevice.swdeviceclose","swdevice/SwDeviceClose"]
old-location: swdevice\swdeviceclose.htm
tech.root: swdevice
ms.assetid: C5E659CD-203A-4021-AB3F-3AFEE2B31E7C
ms.date: 10/11/2021
ms.keywords: SwDeviceClose, SwDeviceClose function, swdevice.swdeviceclose, swdevice/SwDeviceClose
req.header: swdevice.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
 - SwDeviceClose
 - swdevice/SwDeviceClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
 - API-MS-Win-devices-swdevice-l1-1-0.dll
 - API-MS-Win-devices-swdevice-l1-1-1.dll
api_name:
 - SwDeviceClose
---

# SwDeviceClose function


## -description

Closes the software device handle.  When the handle is closed, if the lifetime of the SwDevice is <b>SWDeviceLifetimeHandle</b>, PnP will initiate the process of "unplugging" the device. The device will no longer be reported as a child of its parent device.

## -parameters

### -param hSwDevice [in]

The <b>HSWDEVICE</b> handle to close.

## -remarks

After <b>SwDeviceClose</b> returns, the operating system is guaranteed to not call the <a href="/windows/desktop/api/swdevice/nc-swdevice-sw_device_create_callback">SW_DEVICE_CREATE_CALLBACK</a> callback function, and any calls to Software Device API functions that were in progress are  guaranteed to have completed.

You can call <b>SwDeviceClose</b> at any time even if the callback function hasn't been called yet.

In Windows 8, you can't call <b>SwDeviceClose</b> inside the <a href="/windows/desktop/api/swdevice/nc-swdevice-sw_device_create_callback">SW_DEVICE_CREATE_CALLBACK</a> callback function.  Doing so will cause a deadlock.  Be careful of releasing a ref counted object that will call <b>SwDeviceClose</b> when its destructor runs.  In Windows 8.1, this restriction is lifted, and you can call <b>SwDeviceClose</b> inside the callback function.

By calling <b>SwDeviceClose</b>, if the lifetime of the SwDevice is <b>SWDeviceLifetimeHandle</b>, you initiate the process of "unplugging" the device.  This causes the device to no longer be reported as a child of its parent which causes PnP to issue a "surprise removal" of the device.  The call to <b>SwDeviceClose</b> returns before this removal is complete.  However, you can safely call <a href="/windows/desktop/api/swdevice/nf-swdevice-swdevicecreate">SwDeviceCreate</a> immediately  after <b>SwDeviceClose</b>.  The new create will be queued until the previous removal processing completes, and then the device will be re-created.

PnP removal makes the device "Not present" and does not uninstall the device. PnP removal of a device is the same as unplugging a USB device and all of the persisted property state for the device will remain. If you wish to uninstall the device after calling <b>SwDeviceClose</b>, see <a href="/windows-hardware/drivers/install/how-devices-and-driver-packages-are-uninstalled#uninstalling-the-device">Uninstalling the device</a>.

## -see-also

<a href="/windows/desktop/api/swdevice/nf-swdevice-swdevicecreate">SwDeviceCreate</a>