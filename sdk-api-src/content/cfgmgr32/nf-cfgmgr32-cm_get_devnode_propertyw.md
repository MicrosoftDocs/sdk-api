---
UID: NF:cfgmgr32.CM_Get_DevNode_PropertyW
title: CM_Get_DevNode_PropertyW function (cfgmgr32.h)
description: The CM_Get_DevNode_Property function retrieves a device instance property.
helpviewer_keywords: ["CM_Get_DevNode_Property","CM_Get_DevNode_Property function [Device and Driver Installation]","CM_Get_DevNode_PropertyW","cfgmgr32/CM_Get_DevNode_Property","cfgmgr32/CM_Get_DevNode_PropertyW","devinst.cm_get_devnode_property"]
old-location: devinst\cm_get_devnode_property.htm
tech.root: devinst
ms.assetid: A2EE0C78-13CB-4D9D-B68C-F527CCA2DF26
ms.date: 12/05/2018
ms.keywords: CM_Get_DevNode_Property, CM_Get_DevNode_Property function [Device and Driver Installation], CM_Get_DevNode_PropertyW, cfgmgr32/CM_Get_DevNode_Property, cfgmgr32/CM_Get_DevNode_PropertyW, devinst.cm_get_devnode_property
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows Vista and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Get_DevNode_PropertyW (Unicode) and CM_Get_DevNode_Property (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: CfgMgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Get_DevNode_PropertyW
 - cfgmgr32/CM_Get_DevNode_PropertyW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-devices-config-l1-1-2.dll
 - CfgMgr32.dll
 - API-Ms-Win-Devices-Config-L1-1-0.dll
 - API-Ms-Win-Devices-Config-L1-1-1.dll
api_name:
 - CM_Get_DevNode_Property
 - CM_Get_DevNode_Property
 - CM_Get_DevNode_PropertyW
---

# CM_Get_DevNode_PropertyW function


## -description

The <b>CM_Get_DevNode_Property</b> function retrieves a device instance property.

## -parameters

### -param dnDevInst [in]

Device instance handle that is bound to the local machine.

### -param PropertyKey [in]

Pointer to a <a href="/windows-hardware/drivers/install/devpropkey">DEVPROPKEY</a> structure that represents the device property key of the requested device instance property.

### -param PropertyType [out]

Pointer to a <a href="/windows-hardware/drivers/install/property-data-type-identifiers">DEVPROPTYPE</a>-typed variable that receives the property-data-type identifier of the requested device instance property, where the property-data-type identifier is the bitwise OR between a base-data-type identifier and, if the base-data type is modified, a property-data-type modifier.

### -param PropertyBuffer [out]

Pointer to a buffer that receives the requested device instance property. <b>CM_Get_DevNode_Property</b> retrieves the requested property only if the buffer is large enough to hold all the property value data. The pointer can be NULL.

### -param PropertyBufferSize [in, out]

The size, in bytes, of the <i>PropertyBuffer</i> buffer. If <i>PropertyBuffer</i> is set to NULL, <i>*PropertyBufferSize</i> must be set to zero. As output, if the buffer is not large enough to hold all the property value data, <b>CM_Get_DevNode_Property</b> returns the size of the data, in bytes, in <i>*PropertyBufferSize</i>.

### -param ulFlags [in]

Reserved. Must be set to zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

<b>CM_Get_DevNode_Property</b> is part of the <a href="/windows-hardware/drivers/install/unified-device-property-model--windows-vista-and-later-">Unified Device Property Model</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdevicepropertyw">SetupDiGetDeviceProperty</a>