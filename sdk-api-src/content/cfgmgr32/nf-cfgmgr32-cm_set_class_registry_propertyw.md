---
UID: NF:cfgmgr32.CM_Set_Class_Registry_PropertyW
title: CM_Set_Class_Registry_PropertyW function (cfgmgr32.h)
description: The CM_Set_Class_Registry_Property function sets or deletes a property of a device setup class. (Unicode)
helpviewer_keywords: ["CM_Set_Class_Registry_Property", "CM_Set_Class_Registry_Property function [Device and Driver Installation]", "CM_Set_Class_Registry_PropertyW", "cfgmgr32/CM_Set_Class_Registry_Property", "cfgmgr32/CM_Set_Class_Registry_PropertyW", "cfgmgrfn_e39d0285-7d83-4228-bbf8-f0520c5d6566.xml", "devinst.cm_set_class_registry_property"]
old-location: devinst\cm_set_class_registry_property.htm
tech.root: devinst
ms.assetid: 65e19d09-4a53-439b-9678-f907caf0db5c
ms.date: 12/05/2018
ms.keywords: CM_Set_Class_Registry_Property, CM_Set_Class_Registry_Property function [Device and Driver Installation], CM_Set_Class_Registry_PropertyW, cfgmgr32/CM_Set_Class_Registry_Property, cfgmgr32/CM_Set_Class_Registry_PropertyW, cfgmgrfn_e39d0285-7d83-4228-bbf8-f0520c5d6566.xml, devinst.cm_set_class_registry_property
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Set_Class_Registry_PropertyW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Set_Class_Registry_PropertyW
 - cfgmgr32/CM_Set_Class_Registry_PropertyW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
 - API-Ms-Win-Devices-Config-L1-1-0.dll
 - API-Ms-Win-Devices-Config-L1-1-1.dll
 - CfgMgr32.dll
api_name:
 - CM_Set_Class_Registry_Property
 - CM_Set_Class_Registry_PropertyW
---

# CM_Set_Class_Registry_PropertyW function


## -description

The <b>CM_Set_Class_Registry_Property</b> function sets or deletes a property of a <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a>.

## -parameters

### -param ClassGuid [in]

A pointer to the GUID that represents the device setup class for which to set a property.

### -param ulProperty [in]

A value of type ULONG that identifies the property to set. This value must be one of the CM_CRP_<i>Xxx</i> values that are described for the <i>ulProperty</i> parameter of the <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_class_registry_propertyw">CM_Get_Class_Registry_Property</a> function.

### -param Buffer [in, optional]

A pointer to a buffer that contains the property data. This parameter is optional and can be set to <b>NULL</b>. For more information about setting this parameter and the corresponding <i>ulLength</i> parameter, see the following <b>Remarks</b> section.

### -param ulLength [in]

A value of type ULONG that specifies the size, in bytes, of the property data.

### -param ulFlags [in]

Reserved for internal use only. Must be set to zero.

### -param hMachine [in, optional]

A handle to a remote machine on which to set the specified <a href="/windows-hardware/drivers/install/accessing-device-setup-class-properties">device setup class property</a>. This parameter is optional. If set to <b>NULL</b>, the property is set on the local machine.

## -returns

If the operation succeeds, <b>CM_Set_Class_Registry_Property </b> returns CR_SUCCESS. Otherwise, the function returns one of the other CR_<i>Xxx</i> status codes that are defined in <i>Cfgmgr32.h</i>.

## -remarks

If <i>Buffer</i> is <b>NULL</b>, <i>ulLength</i> must be set to zero.

If <i>ulLength</i> is set to zero, the function deletes the property. 

If <i>Buffer</i> is not set to <b>NULL</b> and <i>ulLength</i> is not set to zero, the supplied value must be the correct size for the REG_<i>Xxx</i> data type for the property that is specified in <i>ulProperty</i>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_class_registry_propertyw">CM_Get_Class_Registry_Property</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassregistrypropertya">SetupDiGetClassRegistryProperty</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetclassregistrypropertya">SetupDiSetClassRegistryProperty</a>
