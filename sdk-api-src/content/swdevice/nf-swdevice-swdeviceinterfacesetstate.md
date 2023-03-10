---
UID: NF:swdevice.SwDeviceInterfaceSetState
title: SwDeviceInterfaceSetState function (swdevice.h)
description: Enables or disables a device interface for a software device.
helpviewer_keywords: ["SwDeviceInterfaceSetState","SwDeviceInterfaceSetState function","swdevice.swdeviceinterfacesetstate","swdevice/SwDeviceInterfaceSetState"]
old-location: swdevice\swdeviceinterfacesetstate.htm
tech.root: swdevice
ms.assetid: 09430CEF-F386-4F08-9D11-78E61C44468D
ms.date: 12/05/2018
ms.keywords: SwDeviceInterfaceSetState, SwDeviceInterfaceSetState function, swdevice.swdeviceinterfacesetstate, swdevice/SwDeviceInterfaceSetState
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
 - SwDeviceInterfaceSetState
 - swdevice/SwDeviceInterfaceSetState
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
 - SwDeviceInterfaceSetState
---

# SwDeviceInterfaceSetState function


## -description

Enables or disables a device interface for a software device.

## -parameters

### -param hSwDevice [in]

The <b>HSWDEVICE</b> handle to the software device to register a device interface for.

### -param pszDeviceInterfaceId [in]

A string that identifies the interface to enable or disable.

### -param fEnabled [in]

A Boolean value that indicates whether to either enable or disable  the interface. <b>TRUE</b> to enable; <b>FALSE</b> to disable.

## -returns

S_OK is returned if <b>SwDeviceInterfaceSetState</b> successfully enabled or disabled the interface; otherwise, an appropriate error value.

## -remarks

You can call <b>SwDeviceInterfaceSetState</b> only after the operating system has called your client app's <a href="/windows/desktop/api/swdevice/nc-swdevice-sw_device_create_callback">SW_DEVICE_CREATE_CALLBACK</a> callback function to notify the client app that device enumeration completed.

You can only use <b>SwDeviceInterfaceSetState</b> to manage interfaces that were previously registered with <a href="/windows/desktop/api/swdevice/nf-swdevice-swdeviceinterfaceregister">SwDeviceInterfaceRegister</a> against the software device that <i>hSwDevice</i> represents.

Client apps use <b>SwDeviceInterfaceSetState</b> to manage the state that they want the interface to have.  The software device changes the actual interface state as needed.  For example, a client app disables and re-enables the interface if the device is re-enumerated for any reason.  The state always tries to reflect the client app’s required state.