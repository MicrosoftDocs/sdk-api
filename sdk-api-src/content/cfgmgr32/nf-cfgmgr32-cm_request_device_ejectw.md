---
UID: NF:cfgmgr32.CM_Request_Device_EjectW
title: CM_Request_Device_EjectW function (cfgmgr32.h)
description: The CM_Request_Device_Eject function prepares a local device instance for safe removal, if the device is removable. If the device can be physically ejected, it will be. (Unicode)
helpviewer_keywords: ["CM_Request_Device_Eject", "CM_Request_Device_Eject function [Device and Driver Installation]", "CM_Request_Device_EjectW", "cfgmgr32/CM_Request_Device_Eject", "cfgmgr32/CM_Request_Device_EjectW", "cfgmgrfn_2c8cc2aa-56fe-4ab3-8063-0db0dcbc3098.xml", "devinst.cm_request_device_eject"]
old-location: devinst\cm_request_device_eject.htm
tech.root: devinst
ms.assetid: a73317c8-52e4-4f2c-855c-94259dc77846
ms.date: 12/05/2018
ms.keywords: CM_Request_Device_Eject, CM_Request_Device_Eject function [Device and Driver Installation], CM_Request_Device_EjectW, cfgmgr32/CM_Request_Device_Eject, cfgmgr32/CM_Request_Device_EjectW, cfgmgrfn_2c8cc2aa-56fe-4ab3-8063-0db0dcbc3098.xml, devinst.cm_request_device_eject
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Request_Device_EjectW (Unicode)
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
 - CM_Request_Device_EjectW
 - cfgmgr32/CM_Request_Device_EjectW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
api_name:
 - CM_Request_Device_Eject
 - CM_Request_Device_EjectW
---

# CM_Request_Device_EjectW function


## -description

The <b>CM_Request_Device_Eject</b> function prepares a local device instance for safe removal, if the device is removable. If the device can be physically ejected, it will be.

## -parameters

### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the local machine.

### -param pVetoType [out, optional]

(<i>Optional</i>.) If not <b>NULL</b>, this points to a location that, if the removal request fails, receives a <a href="/windows/desktop/api/cfg/ne-cfg-pnp_veto_type">PNP_VETO_TYPE</a>-typed value indicating the reason for the failure.

### -param pszVetoName [out, optional]

(<i>Optional</i>.) If not <b>NULL</b>, this is a caller-supplied pointer to a string buffer that receives a text string. The type of information this string provides is dependent on the value received by <i>pVetoType</i>. For information about these strings, see <a href="/windows/desktop/api/cfg/ne-cfg-pnp_veto_type">PNP_VETO_TYPE</a>.

### -param ulNameLength [in]

(<i>Optional</i>.) Caller-supplied value representing the length of the string buffer supplied by <i>pszVetoName</i>. This should be set to MAX_PATH.

### -param ulFlags [in]

Not used.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

If <i>pszVetoName</i> is <b>NULL</b>, the PnP manager displays a message to the user indicating the device was removed or, if the request failed, identifying the reason for the failure. If <i>pszVetoName</i> is not <b>NULL</b>, the PnP manager does not display a message. (Note, however, that for Microsoft Windows 2000 only, the PnP manager displays a message even if <i>pszVetoName</i> is not <b>NULL</b>, if the device's CM_DEVCAP_DOCKDEVICE capability is set.)

Callers of <b>CM_Request_Device_Eject</b> sometimes require <b>SeUndockPrivilege</b> or <b>SeLoadDriverPrivilege</b>, as follows:

<ul>
<li>
If the device's CM_DEVCAP_DOCKDEVICE capability is set (the device is a "dock" device), callers must have <b>SeUndockPrivilege</b>. (<b>SeLoadDriverPrivilege</b> is not required.)

</li>
<li>
If the device's CM_DEVCAP_DOCKDEVICE capability is not set (the device is not a "dock" device), <i>and</i> if the calling process is either not interactive or is running in a multi-user environment in a session not attached to the physical console (such as a remote Terminal Services session), callers of this function must have <b>SeLoadDriverPrivilege</b>. 

</li>
</ul>
Privileges are described in the Microsoft Windows SDK documentation.

For information about using device instance handles that are bound to the local machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew">CM_Query_And_Remove_SubTree</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtree_exw">CM_Query_And_Remove_SubTree_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_device_eject_exw">CM_Request_Device_Eject_Ex</a>
