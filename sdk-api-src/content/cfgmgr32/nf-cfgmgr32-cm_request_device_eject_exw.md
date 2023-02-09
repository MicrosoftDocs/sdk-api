---
UID: NF:cfgmgr32.CM_Request_Device_Eject_ExW
title: CM_Request_Device_Eject_ExW function (cfgmgr32.h)
description: The CM_Request_Device_Eject_Ex function prepares a local or a remote device instance for safe removal, if the device is removable. If the device can be physically ejected, it will be. (Unicode)
helpviewer_keywords: ["CM_Request_Device_Eject_Ex", "CM_Request_Device_Eject_Ex function [Device and Driver Installation]", "CM_Request_Device_Eject_ExW", "cfgmgr32/CM_Request_Device_Eject_Ex", "cfgmgr32/CM_Request_Device_Eject_ExW", "cfgmgrfn_96d92b58-b006-4c9d-bfbd-d5cd620f343f.xml", "devinst.cm_request_device_eject_ex"]
old-location: devinst\cm_request_device_eject_ex.htm
tech.root: devinst
ms.assetid: 80285999-7bcb-4a11-8047-f64cd52cf95a
ms.date: 12/05/2018
ms.keywords: CM_Request_Device_Eject_Ex, CM_Request_Device_Eject_Ex function [Device and Driver Installation], CM_Request_Device_Eject_ExW, cfgmgr32/CM_Request_Device_Eject_Ex, cfgmgr32/CM_Request_Device_Eject_ExW, cfgmgrfn_96d92b58-b006-4c9d-bfbd-d5cd620f343f.xml, devinst.cm_request_device_eject_ex
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Request_Device_Eject_ExW (Unicode)
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
 - CM_Request_Device_Eject_ExW
 - cfgmgr32/CM_Request_Device_Eject_ExW
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
 - CM_Request_Device_Eject_Ex
 - CM_Request_Device_Eject_ExW
---

# CM_Request_Device_Eject_ExW function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw">CM_Request_Device_Eject</a> instead.]

The <b>CM_Request_Device_Eject_Ex</b> function prepares a local or a remote device instance for safe removal, if the device is removable. If the device can be physically ejected, it will be.

## -parameters

### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the machine handle supplied by <i>hMachine</i>.

### -param pVetoType [out, optional]

(<i>Optional</i>.) If not <b>NULL</b>, this points to a location that, if the removal request fails, receives a <a href="/windows/desktop/api/cfg/ne-cfg-pnp_veto_type">PNP_VETO_TYPE</a>-typed value indicating the reason for the failure.

### -param pszVetoName [out, optional]

(<i>Optional</i>.) If not <b>NULL</b>, this is a caller-supplied pointer to a string buffer that receives a text string. The type of information this string provides is dependent on the value received by <i>pVetoType</i>. For information about these strings, see <a href="/windows/desktop/api/cfg/ne-cfg-pnp_veto_type">PNP_VETO_TYPE</a>.

### -param ulNameLength [in]

(<i>Optional</i>.) Caller-supplied value representing the length of the string buffer supplied by <i>pszVetoName</i>. This should be set to MAX_PATH.

### -param ulFlags [in]

Not used.

### -param hMachine [in, optional]

Caller-supplied machine handle to which the caller-supplied device instance handle is bound.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

If <i>pszVetoName</i> is <b>NULL</b>, the PnP manager displays a message to the user indicating the device was removed or, if the request failed, identifying the reason for the failure. If <i>pszVetoName</i> is not <b>NULL</b>, the PnP manager does not display a message. (Note, however, that for Microsoft Windows 2000 only, the PnP manager displays a message even if <i>pszVetoName</i> is not <b>NULL</b>, if the device's CM_DEVCAP_DOCKDEVICE capability is set.)

For remote machines, this function only works for "dock" device instances. That is, the function can only be used remotely to undock a machine. In that case, the caller must have <b>SeUndockPrivilege</b>.

Callers of <b>CM_Request_Eject_Ex</b> sometimes require <b>SeUndockPrivilege</b> or <b>SeLoadDriverPrivilege</b>, as follows:

<ul>
<li>
If the device's CM_DEVCAP_DOCKDEVICE capability is set (the device is a "dock" device), callers must have <b>SeUndockPrivilege</b>. (<b>SeLoadDriverPrivilege</b> is not required.)

</li>
<li>
If the device's CM_DEVCAP_DOCKDEVICE capability is not set (the device is not a "dock" device), <i>and</i> if the calling process is either not interactive or is running in a multi-user environment in a session not attached to the physical console (such as a remote Terminal Services session) callers of this function must have <b>SeLoadDriverPrivilege</b>.

</li>
</ul>
(Privileges are described in the Microsoft Windows SDK documentation.)

For information about using device instance handles that are bound to a local or a remote machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew">CM_Query_And_Remove_SubTree</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtree_exw">CM_Query_And_Remove_SubTree_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw">CM_Request_Device_Eject</a>
