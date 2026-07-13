---
UID: NF:cfgmgr32.CM_Query_And_Remove_SubTreeA
tech.root: devinst 
title: CM_Query_And_Remove_SubTreeA
ms.date: 04/13/2021
targetos: Windows
description: The CM_Query_And_Remove_SubTree function checks whether a device instance and its children can be removed and, if so, it removes them. (ANSI)
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
 - CM_Query_And_Remove_SubTreeA
 - CM_Query_And_Remove_SubTree
f1_keywords:
 - CM_Query_And_Remove_SubTreeA
 - cfgmgr32/CM_Query_And_Remove_SubTreeA
 - CM_Query_And_Remove_SubTree
 - cfgmgr32/CM_Query_And_Remove_SubTree
dev_langs:
 - c++
---

# CM_Query_And_Remove_SubTreeA function

## -description

The <b>CM_Query_And_Remove_SubTree</b> function checks whether a device instance and its children can be removed and, if so, it removes them.

## -parameters

### -param dnAncestor [in]

Caller-supplied device instance handle to the device at the root of the subtree to be removed. This device instance handle is bound to the local machine.

### -param pVetoType [out, optional]

(<i>Optional</i>)  If the caller does not pass <b>NULL</b> and the removal request is vetoed (that is, the function returns CR_REMOVE_VETOED), on return this points to a <a href="/windows/desktop/api/cfg/ne-cfg-pnp_veto_type">PNP_VETO_TYPE</a>-typed value that indicates the reason for the veto.

### -param pszVetoName [out, optional]

(<i>Optional</i>) If the caller does not pass <b>NULL</b> and the removal request is vetoed (that is, the function returns CR_REMOVE_VETOED), on return this points to a text string that is associated with the veto type. The type of information this string provides is dependent on the value received by <i>pVetoType</i>. For information about these strings, see <a href="/windows/desktop/api/cfg/ne-cfg-pnp_veto_type">PNP_VETO_TYPE</a>.

### -param ulNameLength [in]

Caller-supplied value representing the length (number of characters) of the string buffer supplied by <i>pszVetoName</i>. This should be set to MAX_PATH.

### -param ulFlags [in]

A bitwise OR of the caller-supplied flag constants that are described in the <b>Remarks</b> section.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the other CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

The purpose of the <b>CM_Query_And_Remove_SubTree</b> function is to allow an application to prepare a device for safe removal from the local machine. Use this function to remove devices only if a driver has not set the <b>SurpriseRemovalOK</b> member of <a href="/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_device_capabilities">DEVICE_CAPABILITIES</a>. If a driver has set <b>SurpriseRemovalOK</b>, the application should call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_device_ejecta">CM_Request_Device_Eject</a> instead of <b>CM_Query_And_Remove_SubTree</b>.

<b>CM_Query_And_Remove_SubTree</b> supports setting the flags parameter <i>ulFlags</i> with one of the following two flags; these flags apply only if Windows or an installer vetoes the removal of a device:

| Flag | Description |
|------|-------------|
| CM_REMOVE_UI_OK | The function allows a user dialog box to be displayed to indicate the reason for the veto. This is the default flag setting. |
| CM_REMOVE_UI_NOT_OK | The function suppresses the display of a user dialog box that indicates the reason for the veto. |

Beginning with Windows XP, <b>CM_Query_And_Remove_SubTree</b> also supports setting the following additional flag; this flag applies only if the function successfully removes the device instance:


| Flag | Description |
|------|-------------|
| CM_REMOVE_NO_RESTART | If this flag is set, the function configures the device status such that the device cannot be restarted until after the device status is reset. |

The device status is reset by the one of the following:
- Calling [CM_Setup_DevNode](nf-cfgmgr32-cm_setup_devnode.md) for the device and specifying CM_SETUP_DEVNODE_RESET. After the device status is reset in this manner, the device can be restarted by calling [CM_Reenumerate_DevNode](nf-cfgmgr32-cm_reenumerate_devnode.md) for the device instance. After resetting the device status, any other operation that enumerates the device will also restart the device, for example, if the Device Manager is used to reenumerate devices.
- The device is detached and reattached, or the computer is restarted. In this case, the device status will be reset and the device will be restarted.
- If this flag is not set, the device status does not have to be reset. You can restart the removed device by a calling <b>CM_Setup_DevNode</b> for the device and by specifying CM_SETUP_DEVNODE_READY. Any other operation that reenumerates the device will also restart the device. An example of an operation that reenumerates a device is calling <b>CM_Reenumerate_DevNode</b> for the device, detaching and reattaching the device, or restarting the computer. |

Windows applications that do not require the low-level operation <b>CM_Query_And_Remove_SubTree</b> should use the <a href="/windows-hardware/drivers/install/dif-propertychange">DIF_PROPERTYCHANGE</a> request to disable a device instead of using <b>CM_Query_And_Remove_SubTree</b> to remove a device. The DIF_PROPERTYCHANGE request can be used to enable, disable, restart, stop, or change the properties of a device.

Callers of this function must have <b>SeLoadDriverPrivilege</b>. (Privileges are described in the Microsoft Windows SDK documentation.)

For information about using device instance handles that are bound to the local machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>  
<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtree_exa">CM_Query_And_Remove_SubTree_Ex</a>  
<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode">CM_Reenumerate_DevNode</a>  
<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_device_ejecta">CM_Request_Device_Eject</a>  
<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_setup_devnode">CM_Setup_DevNode</a>  
<a href="/windows-hardware/drivers/install/dif-propertychange">DIF_PROPERTYCHANGE</a>  
