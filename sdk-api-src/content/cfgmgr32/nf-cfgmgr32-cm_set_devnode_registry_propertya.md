---
UID: NF:cfgmgr32.CM_Set_DevNode_Registry_PropertyA
tech.root: devinst 
title: CM_Set_DevNode_Registry_PropertyA
ms.date: 04/14/2021
targetos: Windows
description: The CM_Set_DevNode_Registry_Property function sets a specified device property in the registry. (ANSI)
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
req.target-min-winverclnt: Available starting with  Microsoft Windows 2000. 
req.target-min-winversvr: 
req.target-type: Universal 
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
 - CM_Set_DevNode_Registry_PropertyA
 - CM_Set_DevNode_Registry_Property
f1_keywords:
 - CM_Set_DevNode_Registry_PropertyA
 - cfgmgr32/CM_Set_DevNode_Registry_PropertyA
 - CM_Set_DevNode_Registry_Property
 - cfgmgr32/CM_Set_DevNode_Registry_Property
dev_langs:
 - c++
---

# CM_Set_DevNode_Registry_PropertyA function

## -description

The <b>CM_Set_DevNode_Registry_Property</b> function sets a specified device property in the registry.

## -parameters

### -param dnDevInst [in]

A caller-supplied device instance handle that is bound to the local machine.

### -param ulProperty [in]

A CM_DRP_-prefixed constant value that identifies the device property to be set in the registry. These constants are defined in <i>Cfgmgr32.h</i>.

### -param Buffer [in, optional]

A pointer to a caller-supplied buffer that supplies the requested device property, formatted appropriately for the property's data type.

### -param ulLength [in]

The length, in bytes, of the supplied device property.

### -param ulFlags [in]

Not used, must be zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes that are defined in <i>Cfgmgr32.h</i>.

## -remarks

For information about how to use device instance handles that are bound to the local machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>  
<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_set_devnode_registry_propertya">CM_Get_DevNode_Registry_Property</a>  
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya">SetupDiSetDeviceRegistryProperty</a>  
