---
UID: NF:cfgmgr32.CM_Get_DevNode_Status_Ex
title: CM_Get_DevNode_Status_Ex function
author: windows-sdk-content
description: The CM_Get_DevNode_Status_Ex function obtains the status of a device instance from its device node (devnode) on a local or a remote machine's device tree.
old-location: devinst\cm_get_devnode_status_ex.htm
tech.root: devinst
ms.assetid: 3e7dd781-7f99-4c49-bbe1-8d2e63cff553
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CM_Get_DevNode_Status_Ex, CM_Get_DevNode_Status_Ex function [Device and Driver Installation], cfgmgr32/CM_Get_DevNode_Status_Ex, cfgmgrfn_924d6e07-f3bf-4e7d-8342-1b34f4aff24b.xml, devinst.cm_get_devnode_status_ex
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
 - setupapi.dll
api_name:
 - CM_Get_DevNode_Status_Ex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Get_DevNode_Status_Ex function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/7347c142-8bcf-43b3-aef0-5f99e2873560">CM_Get_DevNode_Status</a> instead.]

The <b>CM_Get_DevNode_Status_Ex</b> function obtains the status of a device instance from its device node (<a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">devnode</a>) on a local or a remote machine's <a href="https://msdn.microsoft.com/3220389a-06cc-4a43-8164-b785d1a16365">device tree</a>.


## -parameters




### -param pulStatus [out]

Address of a location to receive status bit flags. The function can set any combination of the DN_-prefixed bit flags defined in <i>Cfg.h</i>.


### -param pulProblemNumber [out]

Address of a location to receive one of the CM_PROB_-prefixed problem values defined in <i>Cfg.h</i>. Used only if DN_HAS_PROBLEM is set in <i>pulStatus</i>.


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



For information about using device instance handles that are bound to a local or a remote machine, see <a href="https://msdn.microsoft.com/bcd46252-6f87-4d49-a24c-81789b0148d9">CM_Get_Child_Ex</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/bcd46252-6f87-4d49-a24c-81789b0148d9">CM_Get_Child_Ex</a>



<a href="https://msdn.microsoft.com/7347c142-8bcf-43b3-aef0-5f99e2873560">CM_Get_DevNode_Status</a>
 

 

