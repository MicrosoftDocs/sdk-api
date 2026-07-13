---
UID: NF:cfgmgr32.CM_Open_DevNode_Key
title: CM_Open_DevNode_Key function (cfgmgr32.h)
description: The CM_Open_DevNode_Key function opens a registry key for device-specific configuration information.
helpviewer_keywords: ["CM_Open_DevNode_Key","CM_Open_DevNode_Key function [Device and Driver Installation]","cfgmgr32/CM_Open_DevNode_Key","cfgmgrfn_951f31d2-624f-4ef2-b954-1b33f9a779e7.xml","devinst.cm_open_devnode_key"]
old-location: devinst\cm_open_devnode_key.htm
tech.root: devinst
ms.assetid: bd69ec16-e8a3-4372-babf-65f8abb7a012
ms.date: 12/05/2018
ms.keywords: CM_Open_DevNode_Key, CM_Open_DevNode_Key function [Device and Driver Installation], cfgmgr32/CM_Open_DevNode_Key, cfgmgrfn_951f31d2-624f-4ef2-b954-1b33f9a779e7.xml, devinst.cm_open_devnode_key
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
 - CM_Open_DevNode_Key
 - cfgmgr32/CM_Open_DevNode_Key
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
 - CM_Open_DevNode_Key
---

# CM_Open_DevNode_Key function


## -description

The <b>CM_Open_DevNode_Key</b> function opens a registry key for device-specific configuration information.

## -parameters

### -param dnDevNode [in]

Caller-supplied device instance handle that is bound to the local machine

### -param samDesired [in]

The registry security access that is required for the requested key.

### -param ulHardwareProfile [in]

The hardware profile to open if <i>ulFlags</i> includes CM_REGISTRY_CONFIG. If this value is zero, the key for the current hardware profile is opened.

### -param Disposition [in]

Specifies how the registry key is to be opened. May be one of the following values:





#### RegDisposition_OpenAlways

Open the key if it exists. Otherwise, create the key.



#### RegDisposition_OpenExisting

Open the key only if it exists.

### -param phkDevice [out]

Pointer to an HKEY that will receive the opened key upon success.

### -param ulFlags [in]

Open device node key flags. Indicates the scope and type of registry storage key to open.  Can be a combination of the following flags:





#### CM_REGISTRY_HARDWARE

Open the device’s hardware key. Do not combine with CM_REGISTRY_SOFTWARE.



#### CM_REGISTRY_SOFTWARE

Open the device’s software key. Do not combine with CM_REGISTRY_HARDWARE.



#### CM_REGISTRY_USER

Open the per-user key for the current user. Do not combine with CM_REGISTRY_CONFIG.



#### CM_REGISTRY_CONFIG

Open the key that stores hardware profile-specific configuration information. Do not combine with CM_REGISTRY_USER.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

Close the handle returned from this function by calling <b>RegCloseKey</b>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_delete_devnode_key">CM_Delete_DevNode_Key</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendevregkey">SetupDiOpenDevRegKey</a>