---
UID: NF:setupapi.SetupDiCreateDeviceInterfaceA
title: SetupDiCreateDeviceInterfaceA function (setupapi.h)
description: The SetupDiCreateDeviceInterface function registers a device interface on a local system or a remote system.helpviewer_keywords: ["SetupDiCreateDeviceInterface","SetupDiCreateDeviceInterface function [Device and Driver Installation]","SetupDiCreateDeviceInterfaceA","SetupDiCreateDeviceInterfaceW","devinst.setupdicreatedeviceinterface","di-rtns_252e73f4-f140-44bf-bd81-abb08a036df7.xml","setupapi/SetupDiCreateDeviceInterface"]
old-location: devinst\setupdicreatedeviceinterface.htm
tech.root: devinst
ms.assetid: e5f78c34-b61c-4fcb-b021-fb8d07c2d841
ms.date: 12/05/2018
ms.keywords: SetupDiCreateDeviceInterface, SetupDiCreateDeviceInterface function [Device and Driver Installation], SetupDiCreateDeviceInterfaceA, SetupDiCreateDeviceInterfaceW, devinst.setupdicreatedeviceinterface, di-rtns_252e73f4-f140-44bf-bd81-abb08a036df7.xml, setupapi/SetupDiCreateDeviceInterface
f1_keywords:
- setupapi/SetupDiCreateDeviceInterface
dev_langs:
- c++
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- LibDef
api_location:
- Setupapi.lib
- Setupapi.dll
api_name:
- SetupDiCreateDeviceInterface - SetupDiCreateDeviceInterfaceA
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupDiCreateDeviceInterfaceA function


## -description


The <b>SetupDiCreateDeviceInterface</b> function registers a device interface on a local system or a remote system. 


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="https://docs.microsoft.com/windows-hardware/drivers/install/device-information-sets">device information set</a>. This set contains a device information element that represents the device for which to register an interface. This handle is typically returned by <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a>. 


### -param DeviceInfoData [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.


### -param InterfaceClassGuid [in]

A pointer to a class GUID that specifies the interface class for the new interface.


### -param ReferenceString [in, optional]

A pointer to a NULL-terminated string that supplies a reference string. This pointer is optional and can be <b>NULL</b>. Reference strings are used only by a few bus drivers that use device interfaces as placeholders for software devices that are created on demand.


### -param CreationFlags [in]

Reserved. Must be zero.


### -param DeviceInterfaceData [out, optional]

A pointer to a caller-initialized <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_device_interface_data">SP_DEVICE_INTERFACE_DATA</a> structure to receive information about the new device interface. This pointer is optional and can be <b>NULL</b>. If the structure is supplied, the caller must set the <b>cbSize</b> member of this structure to <b>sizeof(</b>SP_DEVICE_INTERFACE_DATA<b>)</b> before calling this function. For more information, see the following <b>Remarks</b> section.


## -returns



<b>SetupDiCreateDeviceInterface</b> returns <b>TRUE</b> if the function completed without error. If the function completed with an error, it returns <b>FALSE</b> and the error code for the failure can be retrieved by calling <a href="https://msdn.microsoft.com/library/ms679360(VS.85).aspx">GetLastError</a>.




## -remarks



The caller of this function must be a member of the Administrators group.

<b>SetupDiCreateDeviceInterface</b> registers an interface for a device. If a device has more than one interface, call this function once for each interface being registered. 

If this function successfully registers an interface for the device that corresponds to the specified device information element, it also adds the interface to the interface list that is associated with the device information element in the specified device information set.

Before a registered interface can be used by applications and other system components the interface must be enabled by the driver for the device.

This function creates a registry key for the new device interface. Callers of this function can access nonvolatile storage under this key using <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdiopendeviceinterfaceregkey">SetupDiOpenDeviceInterfaceRegKey</a>.

If <b>SetupDiCreateDeviceInterface</b> successfully creates a new device interface, but the caller-supplied buffer in the <i>DeviceInterfaceData</i> parameter is invalid, this function will return <b>FALSE</b> and a subsequent call to <a href="https://msdn.microsoft.com/library/ms679360(VS.85).aspx">GetLastError</a> will return ERROR_INVALID_USER_BUFFER. However, the function does create and register the new device interface. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdiopendeviceinterfaceregkey">SetupDiOpenDeviceInterfaceRegKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdiremovedeviceinterface">SetupDiRemoveDeviceInterface</a>
 

 

