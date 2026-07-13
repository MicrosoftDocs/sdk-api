---
UID: NF:cfgmgr32.CM_Get_DevNode_Registry_PropertyW
title: CM_Get_DevNode_Registry_PropertyW function (cfgmgr32.h)
description: The CM_Get_DevNode_Registry_Property function retrieves a specified device property from the registry. (Unicode)
helpviewer_keywords: ["CM_Get_DevNode_Registry_Property", "CM_Get_DevNode_Registry_Property function [Device and Driver Installation]", "CM_Get_DevNode_Registry_PropertyW", "cfgmgr32/CM_Get_DevNode_Registry_Property", "cfgmgr32/CM_Get_DevNode_Registry_PropertyW", "cfgmgrfn_f5c0e7d6-81f6-4d0f-bca8-de9c4f51e3d9.xml", "devinst.cm_get_devnode_registry_property"]
old-location: devinst\cm_get_devnode_registry_property.htm
tech.root: devinst
ms.assetid: da0d6970-0f6b-4d92-a384-3799ed3dab55
ms.date: 12/05/2018
ms.keywords: CM_Get_DevNode_Registry_Property, CM_Get_DevNode_Registry_Property function [Device and Driver Installation], CM_Get_DevNode_Registry_PropertyW, cfgmgr32/CM_Get_DevNode_Registry_Property, cfgmgr32/CM_Get_DevNode_Registry_PropertyW, cfgmgrfn_f5c0e7d6-81f6-4d0f-bca8-de9c4f51e3d9.xml, devinst.cm_get_devnode_registry_property
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Microsoft Windows 2000.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Get_DevNode_Registry_PropertyW (Unicode)
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
 - CM_Get_DevNode_Registry_PropertyW
 - cfgmgr32/CM_Get_DevNode_Registry_PropertyW
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
 - CM_Get_DevNode_Registry_Property
 - CM_Get_DevNode_Registry_PropertyW
---

# CM_Get_DevNode_Registry_PropertyW function


## -description

 The <b>CM_Get_DevNode_Registry_Property</b> function retrieves a specified device property from the registry.

## -parameters

### -param dnDevInst [in]

A caller-supplied device instance handle that is bound to the local machine.

### -param ulProperty [in]

A CM_DRP_-prefixed constant value that identifies the device property to be obtained from the registry. These constants are defined in <i>Cfgmgr32.h</i>.

### -param pulRegDataType [out, optional]

Optional, can be <b>NULL</b>. A pointer to a location that receives the registry data type, specified as a REG_-prefixed constant defined in <i>Winnt.h</i>.

### -param Buffer [out, optional]

Optional, can be <b>NULL</b>. A pointer to a caller-supplied buffer that receives the requested device property. If this value is <b>NULL</b>, the function supplies only the length of the requested data in the address pointed to by <i>pulLength</i>.

### -param pulLength [in, out]

A pointer to a ULONG variable into which the function stores the length, in bytes, of the requested device property.

If the <i>Buffer</i> parameter is set to <b>NULL</b>, the ULONG variable must be set to zero.

If the <i>Buffer</i> parameter is not set to <b>NULL</b>, the ULONG variable must be set to the length, in bytes, of the caller-supplied buffer.

### -param ulFlags [in]

Not used, must be zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes that are defined in <i>Cfgmgr32.h</i>.

## -remarks

For information about how to use device instance handles that are bound to the local machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_set_devnode_registry_propertyw">CM_Set_DevNode_Registry_Property</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceregistrypropertya">SetupDiGetDeviceRegistryProperty</a>
