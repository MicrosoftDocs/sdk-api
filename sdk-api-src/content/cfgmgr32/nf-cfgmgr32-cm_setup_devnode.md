---
UID: NF:cfgmgr32.CM_Setup_DevNode
title: CM_Setup_DevNode function (cfgmgr32.h)
description: The CM_Setup_DevNode function restarts a device instance that is not running because there is a problem with the device configuration.
helpviewer_keywords: ["CM_Setup_DevNode","CM_Setup_DevNode function [Device and Driver Installation]","cfgmgr32/CM_Setup_DevNode","cfgmgrfn_e8515529-d4bc-4411-a5cf-18bc4f4d7500.xml","devinst.cm_setup_devnode"]
old-location: devinst\cm_setup_devnode.htm
tech.root: devinst
ms.assetid: 94d0023d-d93f-42da-b2fc-54b9d8831b9b
ms.date: 12/05/2018
ms.keywords: CM_Setup_DevNode, CM_Setup_DevNode function [Device and Driver Installation], cfgmgr32/CM_Setup_DevNode, cfgmgrfn_e8515529-d4bc-4411-a5cf-18bc4f4d7500.xml, devinst.cm_setup_devnode
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
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
req.lib: Cfgmgr32.lib; OneCoreUAP.lib on Windows 10
req.dll: CfgMgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Setup_DevNode
 - cfgmgr32/CM_Setup_DevNode
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
 - CM_Setup_DevNode
---

# CM_Setup_DevNode function


## -description

The <b>CM_Setup_DevNode</b> function restarts a device instance that is not running because there is a problem with the device configuration.

## -parameters

### -param dnDevInst [in]

A device instance handle that is bound to the local system.

### -param ulFlags [in]

One of the following flag values:





#### CM_SETUP_DEVNODE_READY

Restarts a device instance that is not running because of a problem with the device configuration.



#### CM_SETUP_DEVNODE_RESET (Windows XP and later versions of Windows)

Resets a device instance that has the no restart device status flag set. The no restart device status flag is set if a device is removed by calling <b>CM_Query_And_Remove_SubTree</b> or <b>CM_Query_And_Remove_SubTree_Ex</b> and specifying the CM_REMOVE_NO_RESTART flag.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise it returns one of the error codes with "CR_" prefix that are defined in <i>Cfgmgr32.h</i>.

## -remarks

<a href="/windows-hardware/drivers/">Device installation applications</a> should use the <a href="/windows-hardware/drivers/install/dif-propertychange">DIF_PROPERTYCHANGE</a> request to restart a device instead of using this function. The DIF_PROPERTYCHANGE request can be used to enable, disable, restart, stop, or change the properties of a device. 

If a device instance does not have a problem and is already started, <b>CM_Setup_DevNode</b> returns without changing the status of the device instance.

Call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_devnode_status">CM_Get_DevNode_Status</a> or <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_devnode_status_ex">CM_Get_DevNode_Status_Ex</a> to determine the status and problem code for a device instance.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_devnode_status">CM_Get_DevNode_Status</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_devnode_status_ex">CM_Get_DevNode_Status_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew">CM_Query_And_Remove_SubTree</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtree_exw">CM_Query_And_Remove_SubTree_Ex</a>



<a href="/windows-hardware/drivers/install/dif-propertychange">DIF_PROPERTYCHANGE</a>