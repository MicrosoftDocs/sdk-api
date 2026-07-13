---
UID: NF:cfgmgr32.CM_Get_Device_IDA
tech.root: devinst 
title: CM_Get_Device_IDA
ms.date: 04/13/2021
targetos: Windows
description: The CM_Get_Device_ID function retrieves the device instance ID for a specified device instance on the local machine. (ANSI)
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
 - CM_Get_Device_IDA
 - CM_Get_Device_ID
f1_keywords:
 - CM_Get_Device_IDA
 - cfgmgr32/CM_Get_Device_IDA
 - CM_Get_Device_ID
 - cfgmgr32/CM_Get_Device_ID
dev_langs:
 - c++
---

# CM_Get_Device_IDA function

## -description

The <b>CM_Get_Device_ID</b> function retrieves the <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a> for a specified <a href="/windows-hardware/drivers/">device instance</a> on the local machine.

> [!NOTE]
> In Windows Vista and later versions of Windows, the [unified device property model](/windows-hardware/drivers/install/unified-device-property-model--windows-vista-and-later-) uses the [**DEVPKEY_Device_InstanceId**](/windows-hardware/drivers/install/devpkey-device-instanceid) [property key](/windows-hardware/drivers/install/property-keys) to represent the device instance identifier. See [Retrieving a Device Instance Identifier](/windows-hardware/drivers/install/retrieving-a-device-instance-identifier) for details.

## -parameters

### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the local machine.

### -param Buffer [out]

Address of a buffer to receive a device instance ID string. The required buffer size can be obtained by calling <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_size">CM_Get_Device_ID_Size</a>, then incrementing the received value to allow room for the string's terminating <b>NULL</b>.

### -param BufferLen [in]

Caller-supplied length, in characters, of the buffer specified by <i>Buffer</i>.

### -param ulFlags [in]

Not used, must be zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

The function appends a NULL terminator to the supplied device instance ID string, unless the buffer is too small to hold the string. In this case, the function supplies as much of the identifier string as will fit into the buffer, and then returns CR_BUFFER_SMALL. 

For information about device instance IDs, see <a href="/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.

For information about using device instance handles that are bound to the local machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>  
<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_exa">CM_Get_Device_ID_Ex</a>  
