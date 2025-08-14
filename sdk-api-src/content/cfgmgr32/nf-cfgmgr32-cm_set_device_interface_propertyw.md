---
UID: NF:cfgmgr32.CM_Set_Device_Interface_PropertyW
title: CM_Set_Device_Interface_PropertyW function (cfgmgr32.h)
description: The CM_Set_Device_Interface_Property function sets a device property of a device interface.
helpviewer_keywords: ["CM_Set_Device_Interface_Property","CM_Set_Device_Interface_Property function [Device and Driver Installation]","CM_Set_Device_Interface_PropertyW","cfgmgr32/CM_Set_Device_Interface_Property","cfgmgr32/CM_Set_Device_Interface_PropertyW","devinst.cm_set_device_interface_property"]
old-location: devinst\cm_set_device_interface_property.htm
tech.root: devinst
ms.assetid: EB009652-2B20-43C2-A373-AB17F1FBC1B2
ms.date: 12/05/2018
ms.keywords: CM_Set_Device_Interface_Property, CM_Set_Device_Interface_Property function [Device and Driver Installation], CM_Set_Device_Interface_PropertyW, cfgmgr32/CM_Set_Device_Interface_Property, cfgmgr32/CM_Set_Device_Interface_PropertyW, devinst.cm_set_device_interface_property
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows Vista and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Set_Device_Interface_PropertyW (Unicode)
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
 - CM_Set_Device_Interface_PropertyW
 - cfgmgr32/CM_Set_Device_Interface_PropertyW
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
 - CM_Set_Device_Interface_Property
 - CM_Set_Device_Interface_PropertyW
---

# CM_Set_Device_Interface_PropertyW function


## -description

The <b>CM_Set_Device_Interface_Property</b> function sets a device property of a device interface.

## -parameters

### -param pszDeviceInterface [in]

Pointer to a string that identifies the device interface instance for which to set a property for.

### -param PropertyKey [in]

Pointer to a <a href="/windows-hardware/drivers/install/devpropkey">DEVPROPKEY</a> structure that represents the property key of the device interface property to set.

### -param PropertyType [in]

A <a href="/windows-hardware/drivers/install/property-data-type-identifiers">DEVPROPTYPE</a>-typed value that represents the property-data-type identifier for the device interface property. To delete a property, this must be set to DEVPROP_TYPE_EMPTY.

### -param PropertyBuffer [in]

Pointer to a buffer that contains the property value of the device interface property. If either the property or the data is being deleted, this pointer must be set to NULL, and <i>PropertyBufferSize</i> must be set to zero.

### -param PropertyBufferSize [in]

The size, in bytes, of the <i>PropertyBuffer</i> buffer. If <i>PropertyBuffer</i> is set to NULL, <i>PropertyBufferSize</i> must be set to zero.

### -param ulFlags [in]

Reserved. Must be set to zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

<b>CM_Set_Device_Interface_Property</b> is part of the <a href="/windows-hardware/drivers/install/unified-device-property-model--windows-vista-and-later-">Unified Device Property Model</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdeviceinterfacepropertyw">SetupDiSetDeviceInterfaceProperty</a>