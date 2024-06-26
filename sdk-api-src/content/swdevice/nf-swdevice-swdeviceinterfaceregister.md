---
UID: NF:swdevice.SwDeviceInterfaceRegister
title: SwDeviceInterfaceRegister function (swdevice.h)
description: Registers a device interface for a software device and optionally sets properties on that interface.
helpviewer_keywords: ["SwDeviceInterfaceRegister","SwDeviceInterfaceRegister function","swdevice.swdeviceinterfaceregister","swdevice/SwDeviceInterfaceRegister"]
old-location: swdevice\swdeviceinterfaceregister.htm
tech.root: swdevice
ms.assetid: A53FEBC2-E7D7-4DF7-B41C-BBB5A7EE044B
ms.date: 06/20/2024
ms.keywords: SwDeviceInterfaceRegister, SwDeviceInterfaceRegister function, swdevice.swdeviceinterfaceregister, swdevice/SwDeviceInterfaceRegister
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
 - SwDeviceInterfaceRegister
 - swdevice/SwDeviceInterfaceRegister
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
 - SwDeviceInterfaceRegister
---

# SwDeviceInterfaceRegister function


## -description

Registers a device interface for a software device and optionally sets properties on that interface.

## -parameters

### -param hSwDevice [in]

The <b>HSWDEVICE</b> handle to the software device to register a device interface for.

### -param pInterfaceClassGuid [in]

A pointer to the [interface class GUID](/windows-hardware/drivers/install/overview-of-device-interface-classes) that names the contract that this interface implements.

### -param pszReferenceString [in, optional]

An optional reference string that differentiates multiple interfaces of the same class for this device.  This pointer can be <b>NULL</b>.

### -param cPropertyCount [in]

The number of <a href="/previous-versions/windows/hardware/drivers/dn315030(v=vs.85)">DEVPROPERTY</a> structures in the <i>pProperties</i> array.

### -param pProperties [in, optional]

An optional array of <a href="/previous-versions/windows/hardware/drivers/dn315030(v=vs.85)">DEVPROPERTY</a> structures for the properties to set on the interface.  This pointer can be <b>NULL</b>.

Set these properties on the interface after it is created but before a notification that the interface has been created are sent.  For more info, see Remarks.  This pointer can be <b>NULL</b>.

### -param fEnabled [in]

A Boolean value that indicates whether to either enable or disable  the interface. <b>TRUE</b> to enable; <b>FALSE</b> to disable.

### -param ppszDeviceInterfaceId [out, optional]

A pointer to a variable that receives a pointer to the device interface ID for the interface. The caller must free this value with <a href="/windows/desktop/api/swdevice/nf-swdevice-swmemfree">SwMemFree</a>.  This value can be <b>NULL</b> if the client app doesn't need to retrieve the name.

## -returns

S_OK is returned if <b>SwDeviceInterfaceRegister</b> successfully registered the interface; otherwise, an appropriate error value.

## -remarks

You can call <b>SwDeviceInterfaceRegister</b> only after the operating system has called your client app's <a href="/windows/desktop/api/swdevice/nc-swdevice-sw_device_create_callback">SW_DEVICE_CREATE_CALLBACK</a> callback function to notify the client app that device enumeration completed.

You can't call <b>SwDeviceInterfaceRegister</b> for software devices that specify the <a href="/windows/desktop/api/swdevicedef/ns-swdevicedef-sw_device_create_info">SWDeviceCapabilitiesDriverRequired</a> capability.

## -see-also

<a href="/windows/desktop/api/swdevice/nf-swdevice-swmemfree">SwMemFree</a>