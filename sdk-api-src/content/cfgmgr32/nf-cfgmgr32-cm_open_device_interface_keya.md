---
UID: NF:cfgmgr32.CM_Open_Device_Interface_KeyA
title: CM_Open_Device_Interface_KeyA function (cfgmgr32.h)
description: The CM_Open_Device_Interface_Key function opens the registry subkey that is used by applications and drivers to store information that is specific to a device interface. (ANSI)
helpviewer_keywords: ["CM_Open_Device_Interface_KeyA", "cfgmgr32/CM_Open_Device_Interface_KeyA"]
old-location: devinst\cm_open_device_interface_key.htm
tech.root: devinst
ms.assetid: 71802D33-9024-4D7F-9120-8EEFECA53A60
ms.date: 12/05/2018
ms.keywords: CM_Open_Device_Interface_Key, CM_Open_Device_Interface_Key function [Device and Driver Installation], CM_Open_Device_Interface_KeyA, CM_Open_Device_Interface_KeyW, cfgmgr32/CM_Open_Device_Interface_Key, cfgmgr32/CM_Open_Device_Interface_KeyA, cfgmgr32/CM_Open_Device_Interface_KeyW, devinst.cm_open_device_interface_key
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows Vista and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Open_Device_Interface_KeyW (Unicode) and CM_Open_Device_Interface_KeyA (ANSI)
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
 - CM_Open_Device_Interface_KeyA
 - cfgmgr32/CM_Open_Device_Interface_KeyA
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
 - API-MS-Win-Devices-Config-L1-1-0.dll
 - API-MS-Win-Devices-Config-L1-1-1.dll
 - CfgMgr32.dll
api_name:
 - CM_Open_Device_Interface_Key
 - CM_Open_Device_Interface_KeyA
 - CM_Open_Device_Interface_KeyW
---

# CM_Open_Device_Interface_KeyA function


## -description

The <b>CM_Open_Device_Interface_Key</b> function opens the registry subkey that is used by applications and drivers to store information that is specific to a device interface.

## -parameters

### -param pszDeviceInterface [in]

Pointer to a string that identifies the device interface instance to open the registry subkey for.

### -param samDesired [in]

The requested registry security access to the registry subkey.

### -param Disposition [in]

Specifies how the registry key is to be opened. May be one of the following values:





#### RegDisposition_OpenAlways

Open the key if it exists. Otherwise, create the key.



#### RegDisposition_OpenExisting

Open the key only if it exists.

### -param phkDeviceInterface [out]

Pointer to an HKEY that will receive the opened key upon success.

### -param ulFlags [in]

Reserved. Must be set to zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

Close the handle returned from this function by calling <b>RegCloseKey</b>.





> [!NOTE]
> The cfgmgr32.h header defines CM_Open_Device_Interface_Key as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendeviceinterfaceregkey">SetupDiOpenDeviceInterfaceRegKey</a>
