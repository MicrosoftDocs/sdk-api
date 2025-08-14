---
UID: NF:cfgmgr32.CM_Open_Class_KeyA
tech.root: devinst 
title: CM_Open_Class_KeyA
ms.date: 04/13/2021
targetos: Windows
description: The CM_Open_Class_Key function opens the device setup class registry key, the device interface class registry key, or a specific subkey of a class. (ANSI)
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
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows. 
req.target-min-winversvr: 
req.target-type: Desktop 
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
 - CM_Open_Class_KeyA
 - CM_Open_Class_Key
f1_keywords:
 - CM_Open_Class_KeyA
 - cfgmgr32/CM_Open_Class_KeyA
 - CM_Open_Class_Key
 - cfgmgr32/CM_Open_Class_Key
dev_langs:
 - c++
---

# CM_Open_Class_KeyA function

## -description

The <b>CM_Open_Class_Key</b> function opens the device setup class registry key, the device interface class registry key, or a specific subkey of a class.

## -parameters

### -param ClassGuid [in, optional]

Pointer to the GUID of the class whose registry key is to be opened. This parameter is optional and can be NULL. If this parameter is NULL, the root of the class tree is opened.

### -param pszClassName [in, optional]

Reserved. Must be set to NULL.

### -param samDesired [in]

The registry security access for the key to be opened.

### -param Disposition [in]

Specifies how the registry key is to be opened. May be one of the following values:

#### RegDisposition_OpenAlways

Open the key if it exists. Otherwise, create the key.

#### RegDisposition_OpenExisting

Open the key only if it exists.

### -param phkClass [out]

Pointer to an HKEY that will receive the opened key upon success.

### -param ulFlags [in]

Open class key flags:

#### CM_OPEN_CLASS_KEY_INSTALLER

The key to be opened is for a device setup class.

#### CM_OPEN_CLASS_KEY_INTERFACE

The key to be opened is for a device interface class.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

Close the handle returned from this function by calling <b>RegCloseKey</b>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_delete_class_key">CM_Delete_Class_Key</a>  
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopenclassregkeyexa">SetupDiOpenClassRegKeyEx</a>  
