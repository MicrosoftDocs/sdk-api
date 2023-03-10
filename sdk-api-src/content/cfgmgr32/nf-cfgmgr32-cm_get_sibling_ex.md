---
UID: NF:cfgmgr32.CM_Get_Sibling_Ex
title: CM_Get_Sibling_Ex function (cfgmgr32.h)
description: The CM_Get_Sibling_Ex function obtains a device instance handle to the next sibling node of a specified device node, in a local or a remote machine's device tree.
helpviewer_keywords: ["CM_Get_Sibling_Ex","CM_Get_Sibling_Ex function [Device and Driver Installation]","cfgmgr32/CM_Get_Sibling_Ex","cfgmgrfn_f3586db6-4f64-4552-bf60-6e3d440b9138.xml","devinst.cm_get_sibling_ex"]
old-location: devinst\cm_get_sibling_ex.htm
tech.root: devinst
ms.assetid: 6be82983-7ac7-4956-a409-77a371e4d6b4
ms.date: 12/05/2018
ms.keywords: CM_Get_Sibling_Ex, CM_Get_Sibling_Ex function [Device and Driver Installation], cfgmgr32/CM_Get_Sibling_Ex, cfgmgrfn_f3586db6-4f64-4552-bf60-6e3d440b9138.xml, devinst.cm_get_sibling_ex
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
 - CM_Get_Sibling_Ex
 - cfgmgr32/CM_Get_Sibling_Ex
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
 - CM_Get_Sibling_Ex
---

# CM_Get_Sibling_Ex function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_sibling">CM_Get_Sibling</a> instead.]

The <b>CM_Get_Sibling_Ex</b> function obtains a device instance handle to the next sibling node of a specified device node, in a local or a remote machine's <a href="/windows-hardware/drivers/kernel/device-tree">device tree</a>.

## -parameters

### -param pdnDevInst [out]

Caller-supplied pointer to the device instance handle to the sibling node that this function retrieves. The retrieved handle is bound to the machine handle specified by <i>hMachine</i>.

### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the machine handle specified by <i>hMachine</i>.

### -param ulFlags [in]

Not used, must be zero.

### -param hMachine [in, optional]

Caller-supplied machine handle to which the caller-supplied device instance handle is bound.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

To enumerate all children of a device node in the local machine's device tree, first call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a> to obtain a handle to the first child node, then call <b>CM_Get_Sibling_Ex</b> to obtain handles for the rest of the children.

For information about using device instance handles that are bound to a local or a remote machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_sibling">CM_Get_Sibling</a>