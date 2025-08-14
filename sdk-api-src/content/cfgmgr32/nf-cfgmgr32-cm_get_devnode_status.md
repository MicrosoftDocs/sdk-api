---
UID: NF:cfgmgr32.CM_Get_DevNode_Status
title: CM_Get_DevNode_Status function (cfgmgr32.h)
description: The CM_Get_DevNode_Status function obtains the status of a device instance from its device node (devnode) in the local machine's device tree.
helpviewer_keywords: ["CM_Get_DevNode_Status","CM_Get_DevNode_Status function [Device and Driver Installation]","cfgmgr32/CM_Get_DevNode_Status","cfgmgrfn_ac924e13-1a2f-4e48-90fe-1020faf1a0df.xml","devinst.cm_get_devnode_status"]
old-location: devinst\cm_get_devnode_status.htm
tech.root: devinst
ms.assetid: 7347c142-8bcf-43b3-aef0-5f99e2873560
ms.date: 12/05/2018
ms.keywords: CM_Get_DevNode_Status, CM_Get_DevNode_Status function [Device and Driver Installation], cfgmgr32/CM_Get_DevNode_Status, cfgmgrfn_ac924e13-1a2f-4e48-90fe-1020faf1a0df.xml, devinst.cm_get_devnode_status
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
 - CM_Get_DevNode_Status
 - cfgmgr32/CM_Get_DevNode_Status
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
 - CM_Get_DevNode_Status
---

## -description

The <b>CM_Get_DevNode_Status</b> function obtains the status of a device instance from its device node (<a href="/windows-hardware/drivers/">devnode</a>) in the local machine's <a href="/windows-hardware/drivers/kernel/device-tree">device tree</a>.

> [!NOTE]
> In Windows Vista, and later, the [unified device property model](/windows-hardware/drivers/install/unified-device-property-model--windows-vista-and-later-) uses the [**DEVPKEY_Device_DevNodeStatus**](/windows-hardware/drivers/install/devpkey-device-devnodestatus) [property key](/windows-hardware/drivers/install/property-keys) to represent the device instance identifier. For details, see [Retrieving the status and problem code for a device instance](/windows-hardware/drivers/install/retrieving-the-status-and-problem-code-for-a-device-instance).

## -parameters

### -param pulStatus [out]

Address of a location to receive status bit flags. The function can set any combination of the <b>DN_-</b> prefixed bit flags defined in <i>Cfg.h</i>.

### -param pulProblemNumber [out]

Address of a location to receive one of the <b>CM_PROB_</b>-prefixed problem values defined in <i>Cfg.h</i>. Used only if DN_HAS_PROBLEM is set in <i>pulStatus</i>.

### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the local machine.

### -param ulFlags [in]

Not used, must be zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

For information about using device instance handles that are bound to the local machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_devnode_status_ex">CM_Get_DevNode_Status_Ex</a>
