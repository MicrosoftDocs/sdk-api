---
UID: NF:cfgmgr32.CM_Query_And_Remove_SubTree_ExA
tech.root: devinst 
title: CM_Query_And_Remove_SubTree_ExA
ms.date: 04/13/2021
targetos: Windows
description: The CM_Query_And_Remove_SubTree_Ex function checks whether a device instance and its children can be removed and, if so, it removes them. (ANSI)
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
req.target-type: Desktop 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
api_name:
 - CM_Query_And_Remove_SubTree_ExA
 - CM_Query_And_Remove_SubTree_Ex
f1_keywords:
 - CM_Query_And_Remove_SubTree_ExA
 - cfgmgr32/CM_Query_And_Remove_SubTree_ExA
 - CM_Query_And_Remove_SubTree_Ex
 - cfgmgr32/CM_Query_And_Remove_SubTree_Ex
dev_langs:
 - c++
---

# CM_Query_And_Remove_SubTree_ExA function

## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew">CM_Query_And_Remove_SubTree</a> instead.]

The <b>CM_Query_And_Remove_SubTree_Ex</b> function checks whether a device instance and its children can be removed and, if so, it removes them.

## -parameters

### -param dnAncestor [in]

Caller-supplied device instance handle to the device at the root of the subtree to be removed. This device instance handle is bound to the machine handle supplied by <i>hMachine</i>.

### -param pVetoType [out, optional]

(<i>Optional</i>)  If the caller does not pass <b>NULL</b> and the removal request is vetoed (that is, the function returns CR_REMOVE_VETOED), on return this points to a <a href="/windows/desktop/api/cfg/ne-cfg-pnp_veto_type">PNP_VETO_TYPE</a>-typed value that indicates the reason for the veto.

### -param pszVetoName [out, optional]

(<i>Optional</i>) If the caller does not pass <b>NULL</b> and the removal request is vetoed (that is, the function returns CR_REMOVE_VETOED), on return this points to a text string that is associated with the veto type. The type of information this string provides is dependent on the value received by <i>pVetoType</i>. For information about these strings, see <a href="/windows/desktop/api/cfg/ne-cfg-pnp_veto_type">PNP_VETO_TYPE</a>.

### -param ulNameLength [in]

(<i>Optional</i>.) Caller-supplied value representing the length (number of characters) of the string buffer supplied by <i>pszVetoName</i>. This should be set to MAX_PATH.

### -param ulFlags [in]

A bitwise OR of the caller-supplied flag constants that are described in the <b>Remarks</b> section.

### -param hMachine [in, optional]

Caller-supplied machine handle to which the caller-supplied device instance handle is bound.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

The purpose of the <b>CM_Query_And_Remove_SubTree_Ex</b> function is to allow an application to prepare a device for safe removal from a remote machine. Use this function to remove devices only if a driver has not set the <b>SurpriseRemovalOK</b> member of <a href="/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_device_capabilities">DEVICE_CAPABILITIES</a>. If a driver has set <b>SurpriseRemovalOK</b>, the application should call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_device_eject_exa">CM_Request_Device_Eject_Ex</a> instead of <b>CM_Query_And_Remove_SubTree_Ex</b>.

<b>CM_Query_And_Remove_SubTree_Ex</b> supports setting the flags parameter <i>ulFlags</i> with one of the following two flags; these flags apply only if Windows or an installer vetoes the removal of a device:

Beginning with Windows XP, <b>CM_Query_And_Remove_SubTree_Ex</b> also supports setting the following additional flag; this flag applies only if the function successfully removes the device instance:

<a href="/windows-hardware/drivers/">Device installation applications</a> that do not require the low-level operation of <b>CM_Query_And_Remove_SubTree_Ex</b> should use the <a href="/windows-hardware/drivers/install/dif-propertychange">DIF_PROPERTYCHANGE</a> request to disable a device instead of using <b>CM_Query_And_Remove_SubTree_Ex</b> to remove a device. The DIF_PROPERTYCHANGE request can be used to enable, disable, restart, stop, or change the properties of a device.

Callers of this function must have <b>SeLoadDriverPrivilege</b>. (Privileges are described in the Microsoft Windows SDK documentation.)

For information about using device instance handles that are bound to a local or a remote machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>.

Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>  
<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreea">CM_Query_And_Remove_SubTree</a>  
<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode">CM_Reenumerate_DevNode</a>  
<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_device_eject_exa">CM_Request_Device_Eject_Ex</a>  
<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_setup_devnode">CM_Setup_DevNode</a>  
<a href="/windows-hardware/drivers/install/dif-propertychange">DIF_PROPERTYCHANGE</a>  
