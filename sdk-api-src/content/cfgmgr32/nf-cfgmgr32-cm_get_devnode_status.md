---
UID: NF:cfgmgr32.CM_Get_DevNode_Status
title: CM_Get_DevNode_Status function
author: windows-sdk-content
description: The CM_Get_DevNode_Status function obtains the status of a device instance from its device node (devnode) in the local machine's device tree.
old-location: devinst\cm_get_devnode_status.htm
old-project: devinst
ms.assetid: 7347c142-8bcf-43b3-aef0-5f99e2873560
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CM_Get_DevNode_Status, CM_Get_DevNode_Status function [Device and Driver Installation], cfgmgr32/CM_Get_DevNode_Status, cfgmgrfn_ac924e13-1a2f-4e48-90fe-1020faf1a0df.xml, devinst.cm_get_devnode_status
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.redist: 
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
tech.root: 
req.typenames: CM_NOTIFY_ACTION, *PCM_NOTIFY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CfgMgr32.dll
 - API-MS-Win-devices-config-l1-1-0.dll
 - API-MS-Win-devices-config-l1-1-1.dll
api_name:
 - CM_Get_DevNode_Status
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib; OneCoreUAP.lib on Windows 10
req.dll: CfgMgr32.dll
req.irql: 
---

# CM_Get_DevNode_Status function


## -description


The <b>CM_Get_DevNode_Status</b> function obtains the status of a device instance from its device node (<a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">devnode</a>) in the local machine's <a href="https://msdn.microsoft.com/3220389a-06cc-4a43-8164-b785d1a16365">device tree</a>.


## -parameters




### -param pulStatus [out]

Address of a location to receive status bit flags. The function can set any combination of the <b>DN_-</b>prefixed bit flags defined in <i>Cfg.h</i>.


### -param pulProblemNumber [out]

Address of a location to receive one of the <b>CM_PROB_</b>-prefixed problem values defined in <i>Cfg.h</i>. Used only if DN_HAS_PROBLEM is set in <i>pulStatus</i>.


### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the local machine.


### -param ulFlags [in]

Not used, must be zero.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



For information about using device instance handles that are bound to the local machine, see <a href="https://msdn.microsoft.com/b339d794-cbf0-46aa-a106-b2837f797def">CM_Get_Child</a>.




## -see-also




<a href="https://msdn.microsoft.com/b339d794-cbf0-46aa-a106-b2837f797def">CM_Get_Child</a>



<a href="https://msdn.microsoft.com/3e7dd781-7f99-4c49-bbe1-8d2e63cff553">CM_Get_DevNode_Status_Ex</a>
 

 

