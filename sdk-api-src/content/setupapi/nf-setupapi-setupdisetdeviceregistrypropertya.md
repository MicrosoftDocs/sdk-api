---
UID: NF:setupapi.SetupDiSetDeviceRegistryPropertyA
title: SetupDiSetDeviceRegistryPropertyA function (setupapi.h)
description: The SetupDiSetDeviceRegistryProperty function sets a Plug and Play device property for a device. (ANSI)
helpviewer_keywords: ["SetupDiSetDeviceRegistryPropertyA", "di-rtns_c3fa27e1-fbc6-4f82-ab1b-cbf3581c54e4.xml"]
old-location: devinst\setupdisetdeviceregistryproperty.htm
tech.root: devinst
ms.assetid: 2686f416-3eb5-4e6b-87c8-ab10608ab406
ms.date: 12/05/2018
ms.keywords: SetupDiSetDeviceRegistryProperty, SetupDiSetDeviceRegistryProperty function [Device and Driver Installation], SetupDiSetDeviceRegistryPropertyA, SetupDiSetDeviceRegistryPropertyW, devinst.setupdisetdeviceregistryproperty, di-rtns_c3fa27e1-fbc6-4f82-ab1b-cbf3581c54e4.xml, setupapi/SetupDiSetDeviceRegistryProperty
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiSetDeviceRegistryPropertyA
 - setupapi/SetupDiSetDeviceRegistryPropertyA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - ext-ms-win-setupapi-devobj-l1-1-0.dll
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiSetDeviceRegistryProperty - SetupDiSetDeviceRegistryPropertyA
---

# SetupDiSetDeviceRegistryPropertyA function


## -description

The <b>SetupDiSetDeviceRegistryProperty</b> function sets a Plug and Play device property for a device.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a device information element that represents the device for which to set a Plug and Play device property.

### -param DeviceInfoData [in, out]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. If the <b>ClassGuid</b> property is set, <i>DeviceInfoData.</i><b>ClassGuid</b> is set upon return to the new class for the device.

### -param Property [in]

One of the following values, which identifies the property to be set. For descriptions of these values, see <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceregistrypropertya">SetupDiGetDeviceRegistryProperty</a>.

* SPDRP_CONFIGFLAGS
* SPDRP_EXCLUSIVE
* SPDRP_FRIENDLYNAME
* SPDRP_LOCATION_INFORMATION
* SPDRP_LOWERFILTERS
* SPDRP_REMOVAL_POLICY_OVERRIDE
* SPDRP_SECURITY
* SPDRP_SECURITY_SDS
* SPDRP_UI_NUMBER_DESC_FORMAT
* SPDRP_UPPERFILTERS

> [!NOTE]
> SPDRP_HARDWAREID or SPDRP_COMPATIBLEIDS can only be used when *DeviceInfoData* represents a root-enumerated device. For other devices, the bus driver reports hardware and compatible IDs when enumerating a child device after receiving <a href="/windows-hardware/drivers/kernel/irp-mn-query-id">IRP_MN_QUERY_ID</a>.

The following values are reserved for use by the operating system and cannot be used in the *Property* parameter:

* SPDRP_ADDRESS
* SPDRP_BUSNUMBER
* SPDRP_BUSTYPEGUID
* SPDRP_CHARACTERISTICS
* SPDRP_CAPABILITIES
* SPDRP_CLASS
* SPDRP_CLASSGUID
* SPDRP_DEVICE_POWER_DATA
* SPDRP_DEVICEDESC
* SPDRP_DEVTYPE
* SPDRP_DRIVER
* SPDRP_ENUMERATOR_NAME
* SPDRP_INSTALL_STATE
* SPDRP_LEGACYBUSTYPE
* SPDRP_LOCATION_PATHS
* SPDRP_MFG
* SPDRP_PHYSICAL_DEVICE_OBJECT_NAME
* SPDRP_REMOVAL_POLICY
* SPDRP_REMOVAL_POLICY_HW_DEFAULT
* SPDRP_SERVICE
* SPDRP_UI_NUMBER

### -param PropertyBuffer [in, optional]

A pointer to a buffer that contains the new data for the property. If the property is being cleared, then this pointer should be <b>NULL</b> and <i>PropertyBufferSize</i> must be zero.

### -param PropertyBufferSize [in]

The size, in bytes, of <i>PropertyBuffer</i>. If <i>PropertyBuffer</i> is <b>NULL</b>, then this field must be zero.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The caller of this function must be a member of the Administrators group.

The class name property cannot be set because it is based on the corresponding class GUID and is automatically updated when that property is changed. When the ClassGUID property changes, <b>SetupDiSetDeviceRegistryProperty</b> automatically cleans up any software keys associated with the device.





> [!NOTE]
> The setupapi.h header defines SetupDiSetDeviceRegistryProperty as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassregistrypropertya">SetupDiGetClassRegistryProperty</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceregistrypropertya">SetupDiGetDeviceRegistryProperty</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetclassregistrypropertya">SetupDiSetClassRegistryProperty</a>
