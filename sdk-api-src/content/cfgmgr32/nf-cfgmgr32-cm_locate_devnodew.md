---
UID: NF:cfgmgr32.CM_Locate_DevNodeW
title: CM_Locate_DevNodeW function (cfgmgr32.h)
description: The CM_Locate_DevNode function obtains a device instance handle to the device node that is associated with a specified device instance ID on the local machine. (Unicode)
helpviewer_keywords: ["CM_Locate_DevNode", "CM_Locate_DevNode function [Device and Driver Installation]", "CM_Locate_DevNodeW", "cfgmgr32/CM_Locate_DevNode", "cfgmgr32/CM_Locate_DevNodeW", "cfgmgrfn_70e99ef3-9630-4088-8fcb-f6c7123f2cb5.xml", "devinst.cm_locate_devnode"]
old-location: devinst\cm_locate_devnode.htm
tech.root: devinst
ms.assetid: b0bb2510-44be-4598-96ea-9b8fdcc7f7c6
ms.date: 12/05/2018
ms.keywords: CM_Locate_DevNode, CM_Locate_DevNode function [Device and Driver Installation], CM_Locate_DevNodeA, CM_Locate_DevNodeW, cfgmgr32/CM_Locate_DevNode, cfgmgr32/CM_Locate_DevNodeA, cfgmgr32/CM_Locate_DevNodeW, cfgmgrfn_70e99ef3-9630-4088-8fcb-f6c7123f2cb5.xml, devinst.cm_locate_devnode
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Locate_DevNodeW (Unicode) and CM_Locate_DevNodeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: CfgMgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Locate_DevNodeW
 - cfgmgr32/CM_Locate_DevNodeW
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
 - API-MS-Win-Devices-Config-L1-1-0.dll
 - API-MS-Win-Devices-Config-L1-1-1.dll
api_name:
 - CM_Locate_DevNode
 - CM_Locate_DevNodeA
 - CM_Locate_DevNodeW
---

# CM_Locate_DevNodeW function


## -description

The <b>CM_Locate_DevNode</b> function obtains a device instance handle to the device node that is associated with a specified <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a> on the local machine.

## -parameters

### -param pdnDevInst [out]

A pointer to a device instance handle that <b>CM_Locate_DevNode</b> retrieves. The retrieved handle is bound to the local machine.

### -param pDeviceID [in, optional]

A pointer to a NULL-terminated string representing a <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a>. If this value is <b>NULL</b>, or if it points to a zero-length string, the function retrieves a device instance handle to the device at the root of the <a href="/windows-hardware/drivers/kernel/device-tree">device tree</a>.

### -param ulFlags [in]

A variable of ULONG type that supplies one of the following flag values that apply if the caller supplies a device instance identifier:





#### CM_LOCATE_DEVNODE_NORMAL

The function retrieves the device instance handle for the specified device only if the device is currently configured in the device tree. 



#### CM_LOCATE_DEVNODE_PHANTOM

The function retrieves a device instance handle for the specified device if the device is currently configured in the device tree or the device is a <a href="/windows-hardware/drivers/">nonpresent device</a> that is not currently configured in the device tree. 



#### CM_LOCATE_DEVNODE_CANCELREMOVE

The function retrieves a device instance handle for the specified device if the device is currently configured in the device tree or in the process of being removed from the device tree. If the device is in the process of being removed, the function cancels the removal of the device.



#### CM_LOCATE_DEVNODE_NOVALIDATION

Not used.


##### - ulFlags.CM_LOCATE_DEVNODE_CANCELREMOVE

The function retrieves a device instance handle for the specified device if the device is currently configured in the device tree or in the process of being removed from the device tree. If the device is in the process of being removed, the function cancels the removal of the device.


##### - ulFlags.CM_LOCATE_DEVNODE_NORMAL

The function retrieves the device instance handle for the specified device only if the device is currently configured in the device tree. 


##### - ulFlags.CM_LOCATE_DEVNODE_NOVALIDATION

Not used.


##### - ulFlags.CM_LOCATE_DEVNODE_PHANTOM

The function retrieves a device instance handle for the specified device if the device is currently configured in the device tree or the device is a <a href="/windows-hardware/drivers/">nonpresent device</a> that is not currently configured in the device tree.

## -returns

If the operation succeeds, <b>CM_Locate_DevNode</b> returns CR_SUCCESS. Otherwise, the function returns one of the CR_<i>Xxx</i> error codes that are defined in <i>Cfgmgr32.h</i>.

## -remarks

For information about using device instance handles that are bound to the local machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>.





> [!NOTE]
> The cfgmgr32.h header defines CM_Locate_DevNode as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_locate_devnode_exw">CM_Locate_DevNode_Ex</a>
