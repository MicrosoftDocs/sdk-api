---
UID: NF:setupapi.SetupDiSetClassRegistryPropertyA
title: SetupDiSetClassRegistryPropertyA function (setupapi.h)
description: The SetupDiSetClassRegistryProperty function sets a specified device class property in the registry. (ANSI)
helpviewer_keywords: ["SetupDiSetClassRegistryPropertyA", "di-rtns_77b5fc07-42ec-4515-b20c-87cf1c8e4b86.xml"]
old-location: devinst\setupdisetclassregistryproperty.htm
tech.root: devinst
ms.assetid: 78457461-11ef-44ec-aa60-1adf4a48db8c
ms.date: 01/30/2023
ms.keywords: SetupDiSetClassRegistryProperty, SetupDiSetClassRegistryProperty function [Device and Driver Installation], SetupDiSetClassRegistryPropertyA, SetupDiSetClassRegistryPropertyW, devinst.setupdisetclassregistryproperty, di-rtns_77b5fc07-42ec-4515-b20c-87cf1c8e4b86.xml, setupapi/SetupDiSetClassRegistryProperty
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later versions of Windows.
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
 - SetupDiSetClassRegistryPropertyA
 - setupapi/SetupDiSetClassRegistryPropertyA
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
 - SetupDiSetClassRegistryProperty - SetupDiSetClassRegistryPropertyA
---

# SetupDiSetClassRegistryPropertyA function


## -description

The <b>SetupDiSetClassRegistryProperty</b> function sets a specified device class property in the registry.

## -parameters

### -param ClassGuid [in]

A pointer to the GUID that identifies the device class for which a property is to be set.

### -param Property [in]

A value that identifies the property to be set, which must be one of the following:





#### SPCRP_CHARACTERISTICS

The caller supplies flags  that specify the device characteristics for the class. For a list of characteristics flags, see the <i>DeviceCharacteristics</i> parameter of <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-iocreatedevice">IoCreateDevice</a>. Device characteristics should be set when the device class is installed and should not be changed after the device class is installed.



#### SPCRP_DEVTYPE

The caller supplies the device type for the class. For more information, see <a href="/windows-hardware/drivers/kernel/specifying-device-types">Specifying Device Types</a>. Device type should be set when a device class is installed and should not be changed after the device class is installed.



#### SPCRP_EXCLUSIVE

The caller supplies a DWORD value  that specifies whether users can obtain exclusive access to devices for this class. The supplied value is 1 if exclusive access is allowed, or zero otherwise. The exclusive setting for a device should be set when a device class is installed and should not be changed after the device class is installed.



#### SPCRP_LOWERFILTERS

(Windows Vista and later) The caller supplies a REG_MULTI_SZ list of the service names of the lower filter drivers that are installed for the <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a>. For more information about how to install a class filter driver, see <a href="/windows-hardware/drivers/install/installing-a-filter-driver">Installing a Filter Driver</a> and <a href="/windows-hardware/drivers/install/inf-classinstall32-section">INF ClassInstall32 Section</a>. 



#### SPCRP_SECURITY

The caller supplies the device's security descriptor as a SECURITY_DESCRIPTOR structure in self-relative format (described in the Microsoft Windows SDK documentation).



#### SPCRP_SECURITY_SDS

The caller supplies the device's security descriptor as a text string. For information about security descriptor strings, see <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language (Windows)</a>. For information about the format of security descriptor strings, see Security Descriptor Definition Language (Windows).



#### SPCRP_UPPERFILTERS

(Windows Vista and later) The caller supplies a REG_MULTI_SZ list of the service names of the upper filter drivers that are installed for the device setup class. For more information about how to install a class filter driver, see <a href="/windows-hardware/drivers/install/installing-a-filter-driver">Installing a Filter Driver</a> and <a href="/windows-hardware/drivers/install/inf-classinstall32-section">INF ClassInstall32 Section</a>.

### -param PropertyBuffer [in, optional]

A pointer to a buffer that supplies the specified property. This parameter is optional and can be <b>NULL</b>.

### -param PropertyBufferSize [in]

The size, in bytes, of the <i>PropertyBuffer </i> buffer.

### -param MachineName [in, optional]

A pointer to a NULL-terminated string that contains the name of a remote system on which to set the specified device class property. This parameter is optional and can be <b>NULL</b>. If this parameter is <b>NULL</b>, the property is set on the name of the local system.

> [!CAUTION]
> Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.

### -param Reserved

Reserved, must be <b>NULL</b>.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The caller of this function must be a member of the Administrators group.

To determine the data type for a device class property, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassregistrypropertya">SetupDiGetClassRegistryProperty</a>.





> [!NOTE]
> The setupapi.h header defines SetupDiSetClassRegistryProperty as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassregistrypropertya">SetupDiGetClassRegistryProperty</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceregistrypropertya">SetupDiGetDeviceRegistryProperty</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya">SetupDiSetDeviceRegistryProperty</a>
