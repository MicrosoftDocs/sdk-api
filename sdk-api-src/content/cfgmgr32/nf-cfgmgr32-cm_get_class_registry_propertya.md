---
UID: NF:cfgmgr32.CM_Get_Class_Registry_PropertyA
tech.root: devinst 
title: CM_Get_Class_Registry_PropertyA
ms.date: 04/12/2021
targetos: Windows
description: The CM_Get_Class_Registry_Property function retrieves a device setup class property. (ANSI)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: cfgmgr32.h
req.idl: 
req.include-header: Cfgmgr32.h 
req.irql: 
req.kmdf-ver: 
req.lib: Cfgmgr32.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows. 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-devices-config-l1-1-2.dll
 - Cfgmgr32.lib
 - Cfgmgr32.dll
 - API-Ms-Win-Devices-Config-L1-1-0.dll
 - API-Ms-Win-Devices-Config-L1-1-1.dll
 - CfgMgr32.dll
api_name:
 - CM_Get_Class_Registry_PropertyA
 - CM_Get_Class_Registry_Property
f1_keywords:
 - CM_Get_Class_Registry_PropertyA
 - cfgmgr32/CM_Get_Class_Registry_PropertyA
 - CM_Get_Class_Registry_Property
 - cfgmgr32/CM_Get_Class_Registry_Property
dev_langs:
 - c++
---

# CM_Get_Class_Registry_PropertyA function

## -description

The <b>CM_Get_Class_Registry_Property</b> function retrieves a <a href="/windows-hardware/drivers/install/accessing-device-setup-class-properties">device setup class property</a>.

## -parameters

### -param ClassGuid [in]

A pointer to the GUID that represents the <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a> for which to retrieve a property.

### -param ulProperty [in]

A value of type ULONG that identifies the property to be retrieved. This value must be one of the following CM_CRP_<i>Xxx</i> values that are defined in <i>Cfgmgr32.h</i>:

#### CM_CRP_UPPERFILTERS

Represents a REG_MULTI_SZ-type list of strings, where each string contains the name of an upper-level filter driver that is registered for the class.

#### CM_CRP_LOWERFILTERS

Represents a REG_MULTI_SZ-typed list of strings, where each string contains the name of a lower-level filter drivers that is registered for the class.

#### CM_CRP_SECURITY

Represents a value of type REG_BINARY that contains a variable-length, self-relative, <a href="/windows-hardware/drivers/ddi/content/ntifs/ns-ntifs-_security_descriptor">SECURITY_DESCRIPTOR</a> structure.

#### CM_CRP_SECURITY_SDS

Represents a string of type REG_SZ that contains a security descriptor in the <a href="/windows-hardware/drivers/kernel/sddl-for-device-objects">Security Descriptor Definition Language (SDDL)</a> format.

#### CM_CRP_DEVTYPE

Represents a value of type REG_DWORD that indicates the device type for the class. For more information, see <a href="/windows-hardware/drivers/kernel/specifying-device-types">Specifying Device Types</a>.

#### CM_CRP_EXCLUSIVE

Represents a value of type REG_DWORD that indicates whether users can obtain exclusive access to devices for this class. The returned value is 1 if exclusive access is allowed, or zero otherwise.

#### CM_CRP_CHARACTERISTICS

Represents a value of type DWORD that indicates the device characteristics for the class. For a list of characteristics flags, see the <i>DeviceCharacteristics</i> parameter of the <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-iocreatedevice">IoCreateDevice</a> routine.

### -param pulRegDataType [out, optional]

A pointer to a variable of type ULONG that receives the REG_<i>Xxx</i> constant that represents the data type of the requested property. The REG_<i>Xxx</i> constants are defined in <i>Winnt.h</i> and are described in the <b>Type</b> member of the <a href="/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_key_value_basic_information">KEY_VALUE_BASIC_INFORMATION</a> structure. This parameter is optional and can be set to <b>NULL</b>.

### -param Buffer [out]

A pointer to a buffer that receives the requested property data. For more information about this parameter and the buffer-size parameter <i>pulLength</i>, see the following <b>Remarks</b> section.

### -param pulLength [in, out]

A pointer to variable of type ULONG whose value, on input, is the size, in bytes, of the buffer that is supplied by <i>Buffer</i>. On return, <b>CM_Get_Class_Registry_Property </b> sets this variable to the size, in bytes, of the requested property.

### -param ulFlags [in]

Reserved for internal use only. Must be set to zero.

### -param hMachine [in, optional]

A handle to a remote machine from which to retrieve the specified device class property. This parameter is optional, and, if it is set to <b>NULL</b>, the property is retrieved from the local machine.

## -returns

If the operation succeeds, <b>CM_Get_Class_Registry_Property </b> returns CR_SUCCESS. Otherwise, the function returns one of the other CR_<i>Xxx</i> status codes that are defined in <i>Cfgmgr32.h</i>.

## -remarks

To determine the size, in bytes, of a property before attempting to retrieve the property, first call <b>CM_Get_Class_Registry_Property</b>, supplying a <b>NULL</b><i>Buffer</i> pointer and a <b>*</b><i>pulLength </i> value of zero. In response to such a call, the function does not retrieve the property, but sets <b>*</b><i>pulLength</i> to the size of the requested property and returns CR_BUFFER_SMALL. After obtaining the property size, call <b>CM_Get_Class_Registry_Property</b> again, supplying a <i>Buffer</i> pointer to the buffer to receive the property data and supplying the property size in <b>*</b><i>pulLength</i>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_set_class_registry_propertya">CM_Set_Class_Registry_Property</a>  
<a href="/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_key_value_basic_information">KEY_VALUE_BASIC_INFORMATION</a>  
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassregistrypropertya">SetupDiGetClassRegistryProperty</a>  
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetclassregistrypropertya">SetupDiSetClassRegistryProperty</a>  
