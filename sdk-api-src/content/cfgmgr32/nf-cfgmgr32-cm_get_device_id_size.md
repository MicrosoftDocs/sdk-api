---
UID: NF:cfgmgr32.CM_Get_Device_ID_Size
title: CM_Get_Device_ID_Size function (cfgmgr32.h)
description: The CM_Get_Device_ID_Size function retrieves the buffer size required to hold a device instance ID for a device instance on the local machine.
helpviewer_keywords: ["CM_Get_Device_ID_Size","CM_Get_Device_ID_Size function [Device and Driver Installation]","cfgmgr32/CM_Get_Device_ID_Size","cfgmgrfn_7e0a024a-355c-4c4d-8aa2-9ec4078c3a3a.xml","devinst.cm_get_device_id_size"]
old-location: devinst\cm_get_device_id_size.htm
tech.root: devinst
ms.assetid: 3ae682d0-d9fa-4a29-8258-c6f72f1940b7
ms.date: 12/05/2018
ms.keywords: CM_Get_Device_ID_Size, CM_Get_Device_ID_Size function [Device and Driver Installation], cfgmgr32/CM_Get_Device_ID_Size, cfgmgrfn_7e0a024a-355c-4c4d-8aa2-9ec4078c3a3a.xml, devinst.cm_get_device_id_size
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
 - CM_Get_Device_ID_Size
 - cfgmgr32/CM_Get_Device_ID_Size
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
 - CM_Get_Device_ID_Size
---

# CM_Get_Device_ID_Size function


## -description

The <b>CM_Get_Device_ID_Size</b> function retrieves the buffer size required to hold a <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a> for a <a href="/windows-hardware/drivers/">device instance</a> on the local machine.

> [!NOTE]
> In Windows Vista and later versions of Windows, the [unified device property model](/windows-hardware/drivers/install/unified-device-property-model--windows-vista-and-later-) uses the [**DEVPKEY_Device_InstanceId**](/windows-hardware/drivers/install/devpkey-device-instanceid) [property key](/windows-hardware/drivers/install/property-keys) to represent the device instance identifier. See [Retrieving a Device Instance Identifier](/windows-hardware/drivers/install/retrieving-a-device-instance-identifier) for details.

## -parameters

### -param pulLen [out]

Receives a value representing the required buffer size, in characters.

### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the local machine.

### -param ulFlags [in]

Not used, must be zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

The <b>CM_Get_Device_ID_Size</b> function should be called to determine the buffer size required by <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_idw">CM_Get_Device_ID</a>.

The size value supplied in the location pointed to by <i>pulLen</i> is less than MAX_DEVICE_ID_LEN, and does not include the identifier string's terminating <b>NULL</b>. If the specified device instance does not exist, the function supplies a size value of zero.

For information about device instance IDs, see <a href="/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.

For information about using device instance handles that are bound to the local machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_idw">CM_Get_Device_ID</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_size_ex">CM_Get_Device_ID_Size_Ex</a>