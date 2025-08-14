---
UID: NF:cfgmgr32.CM_Delete_Device_Interface_KeyW
title: CM_Delete_Device_Interface_KeyW function (cfgmgr32.h)
description: The CM_Delete_Device_Interface_Key function deletes the registry subkey that is used by applications and drivers to store interface-specific information. (Unicode)
helpviewer_keywords: ["CM_Delete_Device_Interface_Key", "CM_Delete_Device_Interface_Key function [Device and Driver Installation]", "CM_Delete_Device_Interface_KeyW", "cfgmgr32/CM_Delete_Device_Interface_Key", "cfgmgr32/CM_Delete_Device_Interface_KeyW", "devinst.cm_delete_device_interface_key"]
old-location: devinst\cm_delete_device_interface_key.htm
tech.root: devinst
ms.assetid: 3DA5BD50-54AE-47A5-A99C-9E24CB2FA3D6
ms.date: 12/05/2018
ms.keywords: CM_Delete_Device_Interface_Key, CM_Delete_Device_Interface_Key function [Device and Driver Installation], CM_Delete_Device_Interface_KeyW, cfgmgr32/CM_Delete_Device_Interface_Key, cfgmgr32/CM_Delete_Device_Interface_KeyW, devinst.cm_delete_device_interface_key
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows Vista and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Delete_Device_Interface_KeyW (Unicode)
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
 - CM_Delete_Device_Interface_KeyW
 - cfgmgr32/CM_Delete_Device_Interface_KeyW
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
 - CM_Delete_Device_Interface_Key
 - CM_Delete_Device_Interface_KeyW
---

# CM_Delete_Device_Interface_KeyW function


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

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw">CM_Open_Device_Interface_Key</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdideletedeviceinterfaceregkey">SetupDiDeleteDeviceInterfaceRegKey</a>
