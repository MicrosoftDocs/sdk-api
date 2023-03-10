---
UID: NF:cfgmgr32.CM_Set_DevNode_Problem
title: CM_Set_DevNode_Problem function (cfgmgr32.h)
description: The CM_Set_DevNode_Problem function sets a problem code for a device that is installed in a local machine.
helpviewer_keywords: ["CM_Set_DevNode_Problem","CM_Set_DevNode_Problem function [Device and Driver Installation]","cfgmgr32/CM_Set_DevNode_Problem","cfgmgrfn_86b84150-4e79-4eab-83ff-4a7bf5921021.xml","devinst.cm_set_devnode_problem"]
old-location: devinst\cm_set_devnode_problem.htm
tech.root: devinst
ms.assetid: 94bbedfc-aeef-46e7-bcf7-477e274f9d17
ms.date: 12/05/2018
ms.keywords: CM_Set_DevNode_Problem, CM_Set_DevNode_Problem function [Device and Driver Installation], cfgmgr32/CM_Set_DevNode_Problem, cfgmgrfn_86b84150-4e79-4eab-83ff-4a7bf5921021.xml, devinst.cm_set_devnode_problem
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
 - CM_Set_DevNode_Problem
 - cfgmgr32/CM_Set_DevNode_Problem
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
 - CM_Set_DevNode_Problem
---

# CM_Set_DevNode_Problem function


## -description

The <b>CM_Set_DevNode_Problem</b> function sets a problem code for a device that is installed in a local machine.

## -parameters

### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the local machine.

### -param ulProblem [in]

Supplies a problem code, which is zero or one of the CM_PROB_Xxx flags that are described in <a href="/windows-hardware/drivers/install/device-manager-error-messages">Device Manager Error Messages</a>. A value of zero indicates that a problem is not set for the device.

### -param ulFlags [in]

Must be set to zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, the function returns one of the CR_-prefixed error codes that are defined in <i>Cfgmgr32.h</i>.

## -remarks

Use this function to set a problem code for a device that is installed in a local machine. You can also use the following functions to set a device's problem code and to obtain the problem code set for the device:

<ul>
<li>

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_devnode_status">CM_Get_DevNode_Status</a> returns the problem code set for a device installed in a local machine.

</li>
<li>

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_devnode_status_ex">CM_Get_DevNode_Status_Ex</a> returns the problem code set for a device installed in a local or a remote machine.

</li>
<li>

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem_ex">CM_Set_DevNode_Problem_Ex</a> sets a problem code for a device installed in a local or a remote machine.

</li>
</ul>
For information about using device instance handles that are bound to the local machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_devnode_status">CM_Get_DevNode_Status</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_devnode_status_ex">CM_Get_DevNode_Status_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem_ex">CM_Set_DevNode_Problem_Ex</a>