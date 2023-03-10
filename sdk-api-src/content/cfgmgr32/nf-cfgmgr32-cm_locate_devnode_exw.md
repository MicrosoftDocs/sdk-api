---
UID: NF:cfgmgr32.CM_Locate_DevNode_ExW
title: CM_Locate_DevNode_ExW function (cfgmgr32.h)
description: The CM_Locate_DevNode_Ex function obtains a device instance handle to the device node that is associated with a specified device instance ID, on a local machine or a remote machine. (Unicode)
helpviewer_keywords: ["CM_Locate_DevNode_Ex", "CM_Locate_DevNode_Ex function [Device and Driver Installation]", "CM_Locate_DevNode_ExW", "cfgmgr32/CM_Locate_DevNode_Ex", "cfgmgr32/CM_Locate_DevNode_ExW", "cfgmgrfn_33bc675e-9f3a-4485-ac79-1ce406cc43bf.xml", "devinst.cm_locate_devnode_ex"]
old-location: devinst\cm_locate_devnode_ex.htm
tech.root: devinst
ms.assetid: 255d828c-5a71-4d53-80ee-b0a0b3e97414
ms.date: 12/05/2018
ms.keywords: CM_Locate_DevNode_Ex, CM_Locate_DevNode_Ex function [Device and Driver Installation], CM_Locate_DevNode_ExW, cfgmgr32/CM_Locate_DevNode_Ex, cfgmgr32/CM_Locate_DevNode_ExW, cfgmgrfn_33bc675e-9f3a-4485-ac79-1ce406cc43bf.xml, devinst.cm_locate_devnode_ex
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Locate_DevNode_ExW (Unicode)
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
 - CM_Locate_DevNode_ExW
 - cfgmgr32/CM_Locate_DevNode_ExW
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
 - CM_Locate_DevNode_Ex
 - CM_Locate_DevNode_ExW
---

# CM_Locate_DevNode_ExW function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_locate_devnodea">CM_Locate_DevNode</a> instead.]

The <b>CM_Locate_DevNode_Ex</b> function obtains a device instance handle to the device node that is associated with a specified <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a>, on a local machine or a remote machine.

## -parameters

### -param pdnDevInst [out]

A pointer to the device instance handle that this function retrieves. The retrieved handle is bound to the machine handle specified by <i>hMachine</i>.

### -param pDeviceID [in, optional]

A pointer to a NULL-terminated string representing a <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a>. If this value is <b>NULL</b>, or if it points to a zero-length string, the function supplies a device instance handle to the device at the root of the <a href="/windows-hardware/drivers/kernel/device-tree">device tree</a>.

### -param ulFlags [in]

A variable of ULONG type that supplies one of the following flag values that apply if the caller supplies a device instance identifier:





#### CM_LOCATE_DEVNODE_NORMAL

The function retrieves the device instance handle for the specified device only if the device is currently configured in the device tree. 



#### CM_LOCATE_DEVNODE_PHANTOM

The function retrieves a device instance handle for the specified device if the device is currently configured in the device tree or the device is a <a href="/windows-hardware/drivers/">nonpresent device</a> that is not currently configured in the device tree. 



#### CM_LOCATE_DEVNODE_CANCELREMOVE

The function retrieves a device instance handle for the specified device if the device is currently configured in the device tree or in the process of being removed for the device tree. If the device is in the process of being removed, the function cancels the removal of the device.



#### CM_LOCATE_DEVNODE_NOVALIDATION

Not used.

### -param hMachine [in, optional]

A machine handle obtained from a call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>, or a machine handle to which a device information set is bound. The machine handle for a device information set is obtained from the <b>RemoteMachineHandle</b> member of the <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_list_detail_data_a">SP_DEVINFO_LIST_DETAIL_DATA</a> structure for the device information set. Call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinfolistdetaila">SetupDiGetDeviceInfoListDetail</a> to obtain an SP_DEVINFO_LIST_DETAIL_DATA structure.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, <b>CM_Locate_DevNode</b> returns CR_SUCCESS. Otherwise, the function returns one of the CR_-prefixed error codes that are defined in <i>Cfgmgr32.h</i>.

## -remarks

For information about using device instance handles that are bound to a local or a remote machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_locate_devnodea">CM_Locate_DevNode</a>
