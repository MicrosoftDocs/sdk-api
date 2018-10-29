---
UID: NF:cfgmgr32.CM_Set_DevNode_Problem
title: CM_Set_DevNode_Problem function
author: windows-sdk-content
description: The CM_Set_DevNode_Problem function sets a problem code for a device that is installed in a local machine.
old-location: devinst\cm_set_devnode_problem.htm
tech.root: devinst
ms.assetid: 94bbedfc-aeef-46e7-bcf7-477e274f9d17
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CM_Set_DevNode_Problem, CM_Set_DevNode_Problem function [Device and Driver Installation], cfgmgr32/CM_Set_DevNode_Problem, cfgmgrfn_86b84150-4e79-4eab-83ff-4a7bf5921021.xml, devinst.cm_set_devnode_problem
ms.prod: windows-hardware
ms.technology: windows-devices
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
api_name:
 - CM_Set_DevNode_Problem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Set_DevNode_Problem function


## -description


The <b>CM_Set_DevNode_Problem</b> function sets a problem code for a device that is installed in a local machine.


## -parameters




### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the local machine.


### -param ulProblem [in]

Supplies a problem code, which is zero or one of the CM_PROB_Xxx flags that are described in <a href="https://msdn.microsoft.com/library/Ff541422(v=VS.85).aspx">Device Manager Error Messages</a>. A value of zero indicates that a problem is not set for the device. 


### -param ulFlags [in]

Must be set to zero.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, the function returns one of the CR_-prefixed error codes that are defined in <i>Cfgmgr32.h</i>.




## -remarks



Use this function to set a problem code for a device that is installed in a local machine. You can also use the following functions to set a device's problem code and to obtain the problem code set for the device:

<ul>
<li>

<a href="https://msdn.microsoft.com/7347c142-8bcf-43b3-aef0-5f99e2873560">CM_Get_DevNode_Status</a> returns the problem code set for a device installed in a local machine.

</li>
<li>

<a href="https://msdn.microsoft.com/3e7dd781-7f99-4c49-bbe1-8d2e63cff553">CM_Get_DevNode_Status_Ex</a> returns the problem code set for a device installed in a local or a remote machine.

</li>
<li>

<a href="https://msdn.microsoft.com/2e3e2c3a-c507-4cc8-bc2c-823d0b597704">CM_Set_DevNode_Problem_Ex</a> sets a problem code for a device installed in a local or a remote machine.

</li>
</ul>
For information about using device instance handles that are bound to the local machine, see <a href="https://msdn.microsoft.com/b339d794-cbf0-46aa-a106-b2837f797def">CM_Get_Child</a>.




## -see-also




<a href="https://msdn.microsoft.com/b339d794-cbf0-46aa-a106-b2837f797def">CM_Get_Child</a>



<a href="https://msdn.microsoft.com/7347c142-8bcf-43b3-aef0-5f99e2873560">CM_Get_DevNode_Status</a>



<a href="https://msdn.microsoft.com/3e7dd781-7f99-4c49-bbe1-8d2e63cff553">CM_Get_DevNode_Status_Ex</a>



<a href="https://msdn.microsoft.com/2e3e2c3a-c507-4cc8-bc2c-823d0b597704">CM_Set_DevNode_Problem_Ex</a>
 

 

