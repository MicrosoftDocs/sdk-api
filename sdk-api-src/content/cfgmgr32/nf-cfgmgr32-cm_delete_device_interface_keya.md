---
UID: NF:cfgmgr32.CM_Delete_Device_Interface_KeyA
tech.root: devinst
title: CM_Delete_Device_Interface_KeyA
ms.date: 04/12/2021
targetos: Windows
description: The CM_Delete_Device_Interface_Key function deletes the registry subkey that is used by applications and drivers to store interface-specific information. (ANSI)
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
req.target-min-winverclnt: Available in Microsoft Windows Vista and later versions of Windows. 
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
 - CM_Delete_Device_Interface_KeyA
 - CM_Delete_Device_Interface_Key
f1_keywords:
 - CM_Delete_Device_Interface_KeyA
 - cfgmgr32/CM_Delete_Device_Interface_KeyA
 - CM_Delete_Device_Interface_Key
 - cfgmgr32/CM_Delete_Device_Interface_Key
dev_langs:
 - c++
---

# CM_Delete_Device_Interface_KeyA function

## -description

The <b>CM_Delete_Device_Interface_Key</b> function deletes the registry subkey that is used by applications and drivers to store interface-specific information.

## -parameters

### -param pszDeviceInterface [in]

Pointer to a string that identifies the device interface instance of the registry subkey to delete.

### -param ulFlags [in]

Reserved. Must be set to zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keya">CM_Open_Device_Interface_Key</a>  
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdideletedeviceinterfaceregkey">SetupDiDeleteDeviceInterfaceRegKey</a>
