---
UID: NF:cfgmgr32.CM_Get_Depth
title: CM_Get_Depth function (cfgmgr32.h)
description: The CM_Get_Depth function is used to obtain the depth of a specified device node (devnode) within the local machine's device tree.
helpviewer_keywords: ["CM_Get_Depth","CM_Get_Depth function [Device and Driver Installation]","cfgmgr32/CM_Get_Depth","cfgmgrfn_5b045e68-ae42-40ff-a265-693134c95c26.xml","devinst.cm_get_depth"]
old-location: devinst\cm_get_depth.htm
tech.root: devinst
ms.assetid: 4ea0a722-6d44-4690-a2e5-cb39e3fdeb1f
ms.date: 12/05/2018
ms.keywords: CM_Get_Depth, CM_Get_Depth function [Device and Driver Installation], cfgmgr32/CM_Get_Depth, cfgmgrfn_5b045e68-ae42-40ff-a265-693134c95c26.xml, devinst.cm_get_depth
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
 - CM_Get_Depth
 - cfgmgr32/CM_Get_Depth
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
 - CM_Get_Depth
---

# CM_Get_Depth function


## -description

The <b>CM_Get_Depth</b> function is used to obtain the depth of a specified device node (<a href="/windows-hardware/drivers/">devnode</a>) within the local machine's <a href="/windows-hardware/drivers/kernel/device-tree">device tree</a>.

## -parameters

### -param pulDepth [out]

Caller-supplied address of a location to receive a depth value, where zero represents the device tree's root node, one represents the root node's children, and so on.

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



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_depth_ex">CM_Get_Depth_Ex</a>