---
UID: NF:swdevice.SwDevicePropertySet
title: SwDevicePropertySet function
author: windows-sdk-content
description: Sets properties on a software device.
old-location: swdevice\swdevicepropertyset.htm
tech.root: swdevice
ms.assetid: 6EA107FE-F1FD-4D19-82C8-00FE0D98A9EA
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SwDevicePropertySet, SwDevicePropertySet function, swdevice.swdevicepropertyset, swdevice/SwDevicePropertySet
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - SwDevicePropertySet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SwDevicePropertySet function


## -description


Sets properties on a software device.  


## -parameters




### -param hSwDevice [in]

The <b>HSWDEVICE</b> handle to the software device to set properties for. 


### -param cPropertyCount [in]

The number of <a href="https://msdn.microsoft.com/B2B640BC-5DA3-4D9A-95D8-C2EDA09C18FA">DEVPROPERTY</a> structures in the <i>pProperties</i> array.


### -param pProperties [in]

An array of <a href="https://msdn.microsoft.com/B2B640BC-5DA3-4D9A-95D8-C2EDA09C18FA">DEVPROPERTY</a> structures containing the properties to set.


## -returns



S_OK is returned if <b>SwDevicePropertySet</b> successfully set the properties; otherwise, an appropriate error value. 




## -remarks



Typically, only the operating system and Administrators of the computer can set properties on a device, but the creator of a device can call <b>SwDevicePropertySet</b> to set properties on that device even if it isn't the operating system or an Administrator.

You can call <b>SwDevicePropertySet</b> only after the operating system has called your client app's <a href="https://msdn.microsoft.com/3955FA66-EBE2-4710-A873-C5FC8B7DBE2E">SW_DEVICE_CREATE_CALLBACK</a> callback function to notify the client app that device enumeration completed.

There is a subtle difference between properties that are set as part of a <a href="https://msdn.microsoft.com/8274D7D9-D4AD-412E-A9C0-7D4A08C8A14F">SwDeviceCreate</a> call and properties that are later set by calling <b>SwDevicePropertySet</b>.  Properties that are set as part of <b>SwDeviceCreate</b> are stored in memory; if the device is uninstalled or a null driver wipes out the property stores, these properties are written out again by the Software Device API feature when PnP re-enumerates the devices.  This is all transparent to the client.  Properties that are set using <b>SwDevicePropertySet</b> after the enumeration don't persist in memory.  But, if you set a property by using <b>SwDeviceCreate</b>, you can update the value with <b>SwDevicePropertySet</b>, and this update is applied to the in-memory value as well as the persisted store.

You can use <b>SwDevicePropertySet</b> only to set properties in the operating system store for the device.



