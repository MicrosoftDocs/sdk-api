---
UID: NF:cfgmgr32.CM_Get_Child_Ex
title: CM_Get_Child_Ex function (cfgmgr32.h)
description: The CM_Get_Child_Ex function is used to retrieve a device instance handle to the first child node of a specified device node (devnode) in a local or a remote machine's device tree.
helpviewer_keywords: ["CM_Get_Child_Ex","CM_Get_Child_Ex function [Device and Driver Installation]","cfgmgr32/CM_Get_Child_Ex","cfgmgrfn_0f1bca09-50a8-4807-a1d8-79476328b649.xml","devinst.cm_get_child_ex"]
old-location: devinst\cm_get_child_ex.htm
tech.root: devinst
ms.assetid: bcd46252-6f87-4d49-a24c-81789b0148d9
ms.date: 12/05/2018
ms.keywords: CM_Get_Child_Ex, CM_Get_Child_Ex function [Device and Driver Installation], cfgmgr32/CM_Get_Child_Ex, cfgmgrfn_0f1bca09-50a8-4807-a1d8-79476328b649.xml, devinst.cm_get_child_ex
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Get_Child_Ex
 - cfgmgr32/CM_Get_Child_Ex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
api_name:
 - CM_Get_Child_Ex
---

# CM_Get_Child_Ex function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a> instead.]

The <b>CM_Get_Child_Ex</b> function is used to retrieve a device instance handle to the first child node of a specified device node (<a href="/windows-hardware/drivers/">devnode</a>) in a local or a remote machine's <a href="/windows-hardware/drivers/kernel/device-tree">device tree</a>.

## -parameters

### -param pdnDevInst [out]

Caller-supplied pointer to the device instance handle to the child node that this function retrieves. The retrieved handle is bound to the machine handle supplied by <i>hMachine</i>. See the <b>Remarks</b> section.

### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the machine handle supplied by <i>hMachine</i>.

### -param ulFlags [in]

Not used, must be zero.

### -param hMachine [in, optional]

Caller-supplied machine handle to which the caller-supplied device instance handle is bound.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

To enumerate all children of a devnode in a local or a remote machine's device tree, first call <b>CM_Get_Child_Ex</b> to obtain a handle to the first child node, then call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_sibling_ex">CM_Get_Sibling_Ex</a> to obtain handles for the rest of the children.

<b>Using Device Instance Handles</b>

Device instance handle that you use with <a href="/windows/win32/api/cfgmgr32/">PnP configuration manager functions</a> are bound to machine handles, as follows:

<ul>
<li>
All local device instance handles are bound to a NULL-valued local machine handle.

</li>
<li>
If you use a remote machine handle to obtain a device instance handle, the resulting remote device instance handle is bound to the remote machine handle.

</li>
<li>
A device instance handle can be used only with the machine handle to which it is bound. 

</li>
<li>
A device instance handle can be used with another device instance handle only if both device instance handles are bound to the same machine handle.

</li>
</ul>
Use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a> to obtain a remote machine handle for use with remote device instance handles.

To obtain a local or a remote device instance handle, do one of the following. 

<ul>
<li>
Use one of the following functions to retrieve a device instance handle bound to the local machine: <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_locate_devnodea">CM_Locate_DevNode</a>, <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>, <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_parent">CM_Get_Parent</a>, or <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_sibling">CM_Get_Sibling</a>.

</li>
<li>
Use one of the following functions to retrieve a device instance handle bound to a local or a remote machine: <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_locate_devnode_exw">CM_Locate_DevNode_Ex</a>, <b>CM_Get_Child_Ex</b>, <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_parent_ex">CM_Get_Parent_Ex</a>, or <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_sibling_ex">CM_Get_Sibling_Ex</a>.

</li>
</ul>
You can also use the <a href="/windows-hardware/drivers/install/using-device-installation-functions#ddk-update-driver-function-dg">device installation functions</a> to obtain device instance handles. Do the following steps: 

<ol>
<li>
Obtain a device information set. 

</li>
<li>
Obtain an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure for a device instance in the device information set.

</li>
<li>
Obtain the device instance handle for the device instance from the <b>DevInst</b> member of the SP_DEVINFO_DATA structure.

</li>
<li>
Obtain the machine handle to which the device instance handle is bound. A device instance handle obtained from a device information set is bound to the machine handle to which the device information set is bound. You obtain the machine handle for a device information set from the <b>RemoteMachineHandle</b> member of its <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_list_detail_data_a">SP_DEVINFO_LIST_DETAIL_DATA</a> structure. (Call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinfolistdetaila">SetupDiGetDeviceInfoListDetail</a> to obtain an SP_DEVINFO_LIST_DETAIL_DATA structure.)

</li>
</ol>
 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_parent">CM_Get_Parent</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_parent_ex">CM_Get_Parent_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_sibling">CM_Get_Sibling</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_sibling_ex">CM_Get_Sibling_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_locate_devnodea">CM_Locate_DevNode</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_locate_devnode_exw">CM_Locate_DevNode_Ex</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_list_detail_data_a">SP_DEVINFO_LIST_DETAIL_DATA</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinfolistdetaila">SetupDiGetDeviceInfoListDetail</a>