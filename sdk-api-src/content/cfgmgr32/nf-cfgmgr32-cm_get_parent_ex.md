---
UID: NF:cfgmgr32.CM_Get_Parent_Ex
title: CM_Get_Parent_Ex function
author: windows-sdk-content
description: The CM_Get_Parent_Ex function obtains a device instance handle to the parent node of a specified device node (devnode) in a local or a remote machine's device tree.
old-location: devinst\cm_get_parent_ex.htm
old-project: devinst
ms.assetid: ef92f516-e820-41d0-b267-a7e1d01aa7da
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: CM_Get_Parent_Ex, CM_Get_Parent_Ex function [Device and Driver Installation], cfgmgr32/CM_Get_Parent_Ex, cfgmgrfn_880044e3-f794-49d2-9a70-e2a558d8b2de.xml, devinst.cm_get_parent_ex
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CM_NOTIFY_ACTION, *PCM_NOTIFY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
api_name:
 - CM_Get_Parent_Ex
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
---

# CM_Get_Parent_Ex function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/library/windows/hardware/ff538610">CM_Get_Parent</a> instead.]

The <b>CM_Get_Parent_Ex</b> function obtains a device instance handle to the parent node of a specified device node (<a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">devnode</a>) in a local or a remote machine's <a href="https://msdn.microsoft.com/library/windows/hardware/ff543194">device tree</a>.


## -parameters




### -param pdnDevInst [out]

Caller-supplied pointer to the device instance handle to the parent node that this function retrieves. The retrieved handle is bound to the machine handle specified by <i>hMachine</i>.


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



For information about using device instance handles that are bound to a local or a remote machine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff538076">CM_Get_Child_Ex</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538076">CM_Get_Child_Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538610">CM_Get_Parent</a>
 

 

