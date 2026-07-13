---
UID: NF:cfgmgr32.CM_Delete_DevNode_Key
title: CM_Delete_DevNode_Key function (cfgmgr32.h)
description: The CM_Delete_DevNode_Key function deletes the specified user-accessible registry keys that are associated with a device.
helpviewer_keywords: ["CM_Delete_DevNode_Key","CM_Delete_DevNode_Key function [Device and Driver Installation]","cfgmgr32/CM_Delete_DevNode_Key","cfgmgrfn_20a14360-4506-465d-bb5c-79116c3bc78f.xml","devinst.cm_delete_devnode_key"]
old-location: devinst\cm_delete_devnode_key.htm
tech.root: devinst
ms.assetid: a2b6faf3-bd24-416a-b7ea-1ef1b48f965b
ms.date: 12/05/2018
ms.keywords: CM_Delete_DevNode_Key, CM_Delete_DevNode_Key function [Device and Driver Installation], cfgmgr32/CM_Delete_DevNode_Key, cfgmgrfn_20a14360-4506-465d-bb5c-79116c3bc78f.xml, devinst.cm_delete_devnode_key
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
 - CM_Delete_DevNode_Key
 - cfgmgr32/CM_Delete_DevNode_Key
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
 - CM_Delete_DevNode_Key
---

# CM_Delete_DevNode_Key function


## -description

The <b>CM_Delete_DevNode_Key</b> function deletes the specified user-accessible registry keys that are associated with a device.

## -parameters

### -param dnDevNode [in]

Device instance handle that is bound to the local machine.

### -param ulHardwareProfile [in]

The hardware profile to delete if <i>ulFlags</i> includes CM_REGISTRY_CONFIG. If this value is zero, the key for the current hardware profile is deleted. If this value is 0xFFFFFFFF, the registry keys for all hardware profiles are deleted.

### -param ulFlags [in]

Delete device node key flags. Indicates the scope and type of registry storage key to delete.  Can be a combination of the following flags:





#### CM_REGISTRY_HARDWARE

Delete the device’s hardware key. Do not combine with CM_REGISTRY_SOFTWARE.



#### CM_REGISTRY_SOFTWARE

Delete the device’s software key. Do not combine with CM_REGISTRY_HARDWARE.



#### CM_REGISTRY_USER

Delete the per-user key for the current user. Do not combine with CM_REGISTRY_CONFIG.



#### CM_REGISTRY_CONFIG

Delete the key that stores hardware profile-specific configuration information. Do not combine with CM_REGISTRY_USER.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_devnode_key">CM_Open_DevNode_Key</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdideletedevregkey">SetupDiDeleteDevRegKey</a>