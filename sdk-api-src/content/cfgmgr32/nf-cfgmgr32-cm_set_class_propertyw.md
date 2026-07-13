---
UID: NF:cfgmgr32.CM_Set_Class_PropertyW
title: CM_Set_Class_PropertyW function (cfgmgr32.h)
description: The CM_Set_Class_Property function sets a class property for a device setup class or a device interface class.
helpviewer_keywords: ["CM_Set_Class_Property","CM_Set_Class_Property function [Device and Driver Installation]","CM_Set_Class_PropertyW","cfgmgr32/CM_Set_Class_Property","cfgmgr32/CM_Set_Class_PropertyW","devinst.cm_set_class_property"]
old-location: devinst\cm_set_class_property.htm
tech.root: devinst
ms.assetid: BC026F97-4F4B-472F-83C0-FB5114AE1B7A
ms.date: 12/05/2018
ms.keywords: CM_Set_Class_Property, CM_Set_Class_Property function [Device and Driver Installation], CM_Set_Class_PropertyW, cfgmgr32/CM_Set_Class_Property, cfgmgr32/CM_Set_Class_PropertyW, devinst.cm_set_class_property
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows Vista and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Set_Class_PropertyW (Unicode)
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
 - CM_Set_Class_PropertyW
 - cfgmgr32/CM_Set_Class_PropertyW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
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
 - CM_Set_Class_Property
 - CM_Set_Class_PropertyW
---

# CM_Set_Class_PropertyW function


## -description

The <b>CM_Set_Class_Property</b> function sets a class property for a device setup class or a device interface class.

## -parameters

### -param ClassGUID [in]

Pointer to the GUID that identifies the <a href="/windows-hardware/drivers/install/overview-of-device-interface-classes">device interface class</a> or <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a> for which to set a device property. For information about specifying the class type, see the <i>ulFlags</i> parameter.

### -param PropertyKey [in]

Pointer to a <a href="/windows-hardware/drivers/install/devpropkey">DEVPROPKEY</a> structure that represents the property key of the device class property to set.

### -param PropertyType [in]

A <a href="/windows-hardware/drivers/install/property-data-type-identifiers">DEVPROPTYPE</a>-typed value that represents the property-data-type identifier for the device class property. To delete a property, set this to DEVPROP_TYPE_EMPTY.

### -param PropertyBuffer [in]

Pointer to a buffer that contains the property value of the device class property. If either the property or the data is to be deleted, this pointer must be set to NULL, and <i>PropertyBufferSize</i> must be set to zero.

### -param PropertyBufferSize [in]

The size, in bytes, of the <i>PropertyBuffer</i> buffer. If <i>PropertyBuffer</i> is set to NULL, <i>PropertyBufferSize</i> must be set to zero.

### -param ulFlags [in]

Class property flags:





#### CM_CLASS_PROPERTY_INSTALLER

<i>ClassGUID</i> specifies a device setup class. Do not combine with CM_CLASS_PROPERTY_INTERFACE.



#### CM_CLASS_PROPERTY_INTERFACE

<i>ClassGUID</i> specifies a device interface class. Do not combine with CM_CLASS_PROPERTY_INSTALLER.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

<b>CM_Set_Class_Property</b> is part of the <a href="/windows-hardware/drivers/install/unified-device-property-model--windows-vista-and-later-">Unified Device Property Model</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetclasspropertyw">SetupDiSetClassProperty</a>