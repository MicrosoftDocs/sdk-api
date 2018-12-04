---
UID: NF:swdevice.SwDeviceInterfacePropertySet
title: SwDeviceInterfacePropertySet function
author: windows-sdk-content
description: Sets properties on a software device interface.
old-location: swdevice\swdeviceinterfacepropertyset.htm
tech.root: swdevice
ms.assetid: 397E6CAB-EE99-4723-84DB-8C48859E39D8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SwDeviceInterfacePropertySet, SwDeviceInterfacePropertySet function, swdevice.swdeviceinterfacepropertyset, swdevice/SwDeviceInterfacePropertySet
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
 - SwDeviceInterfacePropertySet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SwDeviceInterfacePropertySet function


## -description


Sets properties on a software device interface.  


## -parameters




### -param hSwDevice [in]

The <b>HSWDEVICE</b> handle to the software device of the interface to set properties for. 


### -param pszDeviceInterfaceId [in]

A string that identifies the interface to set properties on.  


### -param cPropertyCount [in]

The number of <a href="https://msdn.microsoft.com/B2B640BC-5DA3-4D9A-95D8-C2EDA09C18FA">DEVPROPERTY</a> structures in the <i>pProperties</i> array.


### -param pProperties [in]

An array of <a href="https://msdn.microsoft.com/B2B640BC-5DA3-4D9A-95D8-C2EDA09C18FA">DEVPROPERTY</a> structures containing the properties to set on the interface.


## -returns



S_OK is returned if <b>SwDeviceInterfacePropertySet</b> successfully set the properties on the interface; otherwise, an appropriate error value. 




## -remarks



Typically, only the operating system and Administrators of the computer can set properties on an interface, but the creator of a device can call <b>SwDeviceInterfacePropertySet</b> to set properties on an interface for that device even if the creator isn't the operating system or an Administrator.

You can call <b>SwDeviceInterfacePropertySet</b> only after the operating system has called your client app's <a href="https://msdn.microsoft.com/3955FA66-EBE2-4710-A873-C5FC8B7DBE2E">SW_DEVICE_CREATE_CALLBACK</a> callback function to notify the client app that device enumeration completed.

There is a subtle difference between properties that are set as part of a <a href="https://msdn.microsoft.com/A53FEBC2-E7D7-4DF7-B41C-BBB5A7EE044B">SwDeviceInterfaceRegister</a> call and properties that are later set by calling <b>SwDeviceInterfacePropertySet</b>.  Properties that are set as part of <b>SwDeviceInterfaceRegister</b> are stored in memory; if the device is uninstalled or a null driver wipes out the property stores, these properties are written out again by the Software Device API feature when PnP re-enumerates the devices.  This is all transparent to the client.  Properties that are set using <b>SwDeviceInterfacePropertySet</b> after the enumeration don't persist in memory.  But, if you set a property by using <b>SwDeviceInterfaceRegister</b>, you can update the value with <b>SwDeviceInterfacePropertySet</b>, and this update is applied to the in-memory value as well as the persisted store.

You can use <b>SwDeviceInterfacePropertySet</b> only to set properties in the operating system store for the interface. 



