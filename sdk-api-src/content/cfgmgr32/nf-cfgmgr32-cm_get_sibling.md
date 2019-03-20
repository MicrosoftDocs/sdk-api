---
UID: NF:cfgmgr32.CM_Get_Sibling
title: CM_Get_Sibling function (cfgmgr32.h)
author: windows-sdk-content
description: The CM_Get_Sibling function obtains a device instance handle to the next sibling node of a specified device node (devnode) in the local machine's device tree.
old-location: devinst\cm_get_sibling.htm
tech.root: devinst
ms.assetid: ac3b7bca-1504-465a-8dcf-dcde9da686a9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CM_Get_Sibling, CM_Get_Sibling function [Device and Driver Installation], cfgmgr32/CM_Get_Sibling, cfgmgrfn_cc0cd494-9629-4915-a0b3-e634516eb62f.xml, devinst.cm_get_sibling
ms.topic: function
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
 - CM_Get_Sibling
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Get_Sibling function


## -description


The <b>CM_Get_Sibling</b> function obtains a device instance handle to the next sibling node of a specified device node (<a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">devnode</a>) in the local machine's <a href="https://msdn.microsoft.com/3220389a-06cc-4a43-8164-b785d1a16365">device tree</a>.


## -parameters




### -param pdnDevInst [out]

Caller-supplied pointer to the device instance handle to the sibling node that this function retrieves. The retrieved handle is bound to the local machine.


### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the local machine.


### -param ulFlags [in]

Not used, must be zero.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



To enumerate all children of a devnode in the local machine's device tree, first call <a href="https://msdn.microsoft.com/b339d794-cbf0-46aa-a106-b2837f797def">CM_Get_Child</a> to obtain a handle to the first child node, then call <b>CM_Get_Sibling</b> to obtain handles for the rest of the children.

For information about using device instance handles that are bound to the local machine, see <a href="https://msdn.microsoft.com/b339d794-cbf0-46aa-a106-b2837f797def">CM_Get_Child</a>.




## -see-also




<a href="https://msdn.microsoft.com/b339d794-cbf0-46aa-a106-b2837f797def">CM_Get_Child</a>



<a href="https://msdn.microsoft.com/6be82983-7ac7-4956-a409-77a371e4d6b4">CM_Get_Sibling_Ex</a>
 

 

