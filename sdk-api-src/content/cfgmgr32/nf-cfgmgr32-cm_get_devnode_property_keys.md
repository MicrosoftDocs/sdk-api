---
UID: NF:cfgmgr32.CM_Get_DevNode_Property_Keys
title: CM_Get_DevNode_Property_Keys function (cfgmgr32.h)
description: The CM_Get_DevNode_Property_Keys function retrieves an array of the device property keys that represent the device properties that are set for a device instance.
helpviewer_keywords: ["CM_Get_DevNode_Property_Keys","CM_Get_DevNode_Property_Keys function [Device and Driver Installation]","cfgmgr32/CM_Get_DevNode_Property_Keys","devinst.cm_get_devnode_property_keys"]
old-location: devinst\cm_get_devnode_property_keys.htm
tech.root: devinst
ms.assetid: 3476FAA7-32EA-43A9-B7CF-3938F08E0AD1
ms.date: 12/05/2018
ms.keywords: CM_Get_DevNode_Property_Keys, CM_Get_DevNode_Property_Keys function [Device and Driver Installation], cfgmgr32/CM_Get_DevNode_Property_Keys, devinst.cm_get_devnode_property_keys
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows Vista and later versions of Windows.
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
req.lib: Cfgmgr32.lib; OneCoreUAP.lib on Windows 10
req.dll: CfgMgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Get_DevNode_Property_Keys
 - cfgmgr32/CM_Get_DevNode_Property_Keys
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
 - API-MS-Win-devices-config-l1-1-0.dll
 - API-MS-Win-devices-config-l1-1-1.dll
api_name:
 - CM_Get_DevNode_Property_Keys
---

# CM_Get_DevNode_Property_Keys function


## -description

The <b>CM_Get_DevNode_Property_Keys</b> function retrieves an array of the device property keys that represent the device properties that are set for a device instance.

## -parameters

### -param dnDevInst [in]

Device instance handle that is bound to the local machine.

### -param PropertyKeyArray [out, optional]

Pointer to a buffer that receives an array of <a href="/windows-hardware/drivers/install/devpropkey">DEVPROPKEY</a>-typed values, where each value is a device property key that represents a device property that is set for the device instance. The pointer is optional and can be NULL.

### -param PropertyKeyCount [in, out]

The size, in <a href="/windows-hardware/drivers/install/devpropkey">DEVPROPKEY</a>-typed units, of the <i>PropertyKeyArray</i> buffer. If <i>PropertyKeyArray</i> is set to NULL, <i>*PropertyKeyCount</i> must be set to zero. As output, If <i>PropertyKeyArray</i> is not large enough to hold all the property key data, <b>CM_Get_DevNode_Property_Keys</b> returns the count of the keys in <i>*PropertyKeyCount</i>.

### -param ulFlags [in]

Reserved. Must be set to zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

<b>CM_Get_DevNode_Property_Keys</b> is part of the <a href="/windows-hardware/drivers/install/unified-device-property-model--windows-vista-and-later-">Unified Device Property Model</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdevicepropertykeys">SetupDiGetDevicePropertyKeys</a>