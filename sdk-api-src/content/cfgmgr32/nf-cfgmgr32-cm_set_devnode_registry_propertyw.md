---
UID: NF:cfgmgr32.CM_Set_DevNode_Registry_PropertyW
title: CM_Set_DevNode_Registry_PropertyW function (cfgmgr32.h)
description: The CM_Set_DevNode_Registry_Property function sets a specified device property in the registry. (Unicode)
helpviewer_keywords: ["CM_Set_DevNode_Registry_Property", "CM_Set_DevNode_Registry_Property function [Device and Driver Installation]", "CM_Set_DevNode_Registry_PropertyW", "cfgmgr32/CM_Set_DevNode_Registry_Property", "cfgmgr32/CM_Set_DevNode_Registry_PropertyW", "cfgmgrfn_7ad90f32-c153-4ba1-b2bf-c5f86da160ff.xml", "devinst.cm_set_devnode_registry_property"]
old-location: devinst\cm_set_devnode_registry_property.htm
tech.root: devinst
ms.assetid: 0f1b6883-c232-4f51-8f5c-5e9c00708727
ms.date: 12/05/2018
ms.keywords: CM_Set_DevNode_Registry_Property, CM_Set_DevNode_Registry_Property function [Device and Driver Installation], CM_Set_DevNode_Registry_PropertyW, cfgmgr32/CM_Set_DevNode_Registry_Property, cfgmgr32/CM_Set_DevNode_Registry_PropertyW, cfgmgrfn_7ad90f32-c153-4ba1-b2bf-c5f86da160ff.xml, devinst.cm_set_devnode_registry_property
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with  Microsoft Windows 2000.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Set_DevNode_Registry_PropertyW (Unicode)
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
 - CM_Set_DevNode_Registry_PropertyW
 - cfgmgr32/CM_Set_DevNode_Registry_PropertyW
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
 - CM_Set_DevNode_Registry_Property
 - CM_Set_DevNode_Registry_PropertyW
---

# CM_Set_DevNode_Registry_PropertyW function


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



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_set_devnode_registry_propertyw">CM_Get_DevNode_Registry_Property</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya">SetupDiSetDeviceRegistryProperty</a>
