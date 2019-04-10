---
UID: NF:swdevice.SwDeviceClose
title: SwDeviceClose function (swdevice.h)
author: windows-sdk-content
description: Closes the software device handle. When the handle is closed, PnP will initiate the process of removing the device.
old-location: swdevice\swdeviceclose.htm
tech.root: swdevice
ms.assetid: C5E659CD-203A-4021-AB3F-3AFEE2B31E7C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SwDeviceClose, SwDeviceClose function, swdevice.swdeviceclose, swdevice/SwDeviceClose
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SwDeviceClose function


## -description


Closes the software device handle.  When the handle is closed, PnP will initiate the process of removing the device.


## -parameters




### -param hSwDevice [in]

The <b>HSWDEVICE</b> handle to close.


## -returns



None




## -remarks



After <b>SwDeviceClose</b> returns, the operating system is guaranteed to not call the <a href="https://msdn.microsoft.com/3955FA66-EBE2-4710-A873-C5FC8B7DBE2E">SW_DEVICE_CREATE_CALLBACK</a> callback function, and any calls to Software Device API functions that were in progress are  guaranteed to have completed.

You can call <b>SwDeviceClose</b> at any time even if the callback function hasn't been called yet.

In Windows 8, you can't call <b>SwDeviceClose</b> inside the <a href="https://msdn.microsoft.com/3955FA66-EBE2-4710-A873-C5FC8B7DBE2E">SW_DEVICE_CREATE_CALLBACK</a> callback function.  Doing so will cause a deadlock.  Be careful of releasing a ref counted object that will call <b>SwDeviceClose</b> when its destructor runs.  In Windows 8.1, this restriction is lifted, and you can call <b>SwDeviceClose</b> inside the callback function.

By calling <b>SwDeviceClose</b>, you initiate the process of removing a device from PnP.  The call to <b>SwDeviceClose</b> returns before this removal is complete.  But you can safely call <a href="https://msdn.microsoft.com/8274D7D9-D4AD-412E-A9C0-7D4A08C8A14F">SwDeviceCreate</a> immediately  after <b>SwDeviceClose</b>.  The new create will be queued until the previous removal processing completes, and then the device will be re-created.

PnP removal makes the device "Not present." PnP removal of a device is the same us unplugging a USB device.  All the persisted property state for the device remains in memory.




## -see-also




<a href="https://msdn.microsoft.com/8274D7D9-D4AD-412E-A9C0-7D4A08C8A14F">SwDeviceCreate</a>
 

 

