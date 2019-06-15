---
UID: NF:cfgmgr32.CM_Get_Sibling
title: CM_Get_Sibling function (cfgmgr32.h)
author: windows-sdk-content
description: The CM_Get_Sibling function obtains a device instance handle to the next sibling node of a specified device node (devnode) in the local machine's device tree.
old-location: devinst\cm_get_sibling.htm
tech.root: devinst
ms.assetid: ac3b7bca-1504-465a-8dcf-dcde9da686a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CM_Get_Sibling, CM_Get_Sibling function [Device and Driver Installation], cfgmgr32/CM_Get_Sibling, cfgmgrfn_cc0cd494-9629-4915-a0b3-e634516eb62f.xml, devinst.cm_get_sibling
ms.topic: function
f1_keywords: ["cfgmgr32/CM_Get_Sibling"]
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
ms.custom: 19H1
---

# CM_Get_Sibling function


## -description


The <b>CM_Get_Sibling</b> function obtains a device instance handle to the next sibling node of a specified device node (<a href="https://docs.microsoft.com/windows-hardware/drivers/">devnode</a>) in the local machine's <a href="https://docs.microsoft.com/windows-hardware/drivers/kernel/device-tree">device tree</a>.


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



To enumerate all children of a devnode in the local machine's device tree, first call <a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a> to obtain a handle to the first child node, then call <b>CM_Get_Sibling</b> to obtain handles for the rest of the children.

For information about using device instance handles that are bound to the local machine, see <a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_sibling_ex">CM_Get_Sibling_Ex</a>
 

 

