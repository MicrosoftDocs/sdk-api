---
UID: NF:cfgmgr32.CM_Get_Child
title: CM_Get_Child function
author: windows-sdk-content
description: The CM_Get_Child function is used to retrieve a device instance handle to the first child node of a specified device node (devnode) in the local machine's device tree.
old-location: devinst\cm_get_child.htm
old-project: devinst
ms.assetid: b339d794-cbf0-46aa-a106-b2837f797def
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CM_Get_Child, CM_Get_Child function [Device and Driver Installation], cfgmgr32/CM_Get_Child, cfgmgrfn_ca4f152f-3a57-4e04-b9b8-c9ed65b600f8.xml, devinst.cm_get_child
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
 - CM_Get_Child
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib; OneCoreUAP.lib on Windows 10
req.dll: CfgMgr32.dll
req.irql: 
---

# CM_Get_Child function


## -description


The <b>CM_Get_Child</b> function is used to retrieve a device instance handle to the first child node of a specified device node (<a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">devnode</a>) in the local machine's <a href="https://msdn.microsoft.com/3220389a-06cc-4a43-8164-b785d1a16365">device tree</a>.


## -parameters




### -param pdnDevInst [out]

Caller-supplied pointer to the device instance handle to the child node that this function retrieves. The retrieved handle is bound to the local machine. See the <b>Remarks</b> section.


### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the local machine.


### -param ulFlags [in]

Not used, must be zero.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



To enumerate all children of a devnode in the local machine's device tree, first call <b>CM_Get_Child</b> to obtain a device instance handle to the first child node, then call <a href="https://msdn.microsoft.com/ac3b7bca-1504-465a-8dcf-dcde9da686a9">CM_Get_Sibling</a> to obtain handles for the rest of the children.

<b>Using Device Instance Handles</b>

Device instance handle that you use with <a href="https://msdn.microsoft.com/07e4b970-3105-440a-811a-8863ff21f9b6">PnP configuration manager functions</a> are bound to machine handles, as follows:

<ul>
<li>
All local device instance handles are bound to a NULL-valued local machine handle.

</li>
<li>
If you use a remote machine handle to obtain a device instance handle, the resulting remote device instance handle is bound to the remote machine handle.

</li>
<li>
A device instance handle can be used only with the machine handle to which it is bound. 

</li>
<li>
A device instance handle can be used with another device instance handle only if both device instance handles are bound to the same machine handle.

</li>
</ul>
To obtain a device instance handle that is bound to the local machine, do one of the following.

<ul>
<li>
Use one of the following functions that retrieve only local device instance handles: <a href="https://msdn.microsoft.com/b0bb2510-44be-4598-96ea-9b8fdcc7f7c6">CM_Locate_DevNode</a>, <b>CM_Get_Child</b>, <a href="https://msdn.microsoft.com/e9d1db59-e9fb-4704-81f6-86523397c114">CM_Get_Parent</a>, or <a href="https://msdn.microsoft.com/ac3b7bca-1504-465a-8dcf-dcde9da686a9">CM_Get_Sibling</a>.

</li>
<li>
Use one of the following functions, which retrieves local and remote device instance handles, to retrieve a local device instance handle: <a href="https://msdn.microsoft.com/255d828c-5a71-4d53-80ee-b0a0b3e97414">CM_Locate_DevNode_Ex</a>, <a href="https://msdn.microsoft.com/bcd46252-6f87-4d49-a24c-81789b0148d9">CM_Get_Child_Ex</a>, <a href="https://msdn.microsoft.com/ef92f516-e820-41d0-b267-a7e1d01aa7da">CM_Get_Parent_Ex</a>, or <a href="https://msdn.microsoft.com/6be82983-7ac7-4956-a409-77a371e4d6b4">CM_Get_Sibling_Ex</a>.

</li>
</ul>
You can also use the <a href="https://msdn.microsoft.com/e67fc124-6127-492b-b975-4243b742a0ce">device installation functions</a> to obtain local device instance handles from a device information set that is bound to the local machine. Do the following steps: 

<ol>
<li>
Obtain a device information set that is bound to the local machine. (A device instance handle obtained from a device information set is bound to the machine handle to which the device information set is bound. You obtain the machine handle for a device information set from the <b>RemoteMachineHandle</b> member of its <a href="https://msdn.microsoft.com/03e6c137-5a7f-443d-878f-5e5c6642dde9">SP_DEVINFO_LIST_DETAIL_DATA</a> structure. For a local device information set that is bound to the local machine, the value of <b>RemoteMachineHandle</b> is <b>NULL</b>. Call <a href="https://msdn.microsoft.com/3f624882-9ccc-4be1-92aa-8bba9f0022ea">SetupDiGetDeviceInfoListDetail</a> to obtain an SP_DEVINFO_LIST_DETAIL_DATA structure.)

</li>
<li>
Obtain an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure for a device instance in the device information set.

</li>
<li>
Obtain the device instance handle for the device instance from the <b>DevInst</b> member of the SP_DEVINFO_DATA structure.

</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/bcd46252-6f87-4d49-a24c-81789b0148d9">CM_Get_Child_Ex</a>



<a href="https://msdn.microsoft.com/e9d1db59-e9fb-4704-81f6-86523397c114">CM_Get_Parent</a>



<a href="https://msdn.microsoft.com/ef92f516-e820-41d0-b267-a7e1d01aa7da">CM_Get_Parent_Ex</a>



<a href="https://msdn.microsoft.com/ac3b7bca-1504-465a-8dcf-dcde9da686a9">CM_Get_Sibling</a>



<a href="https://msdn.microsoft.com/6be82983-7ac7-4956-a409-77a371e4d6b4">CM_Get_Sibling_Ex</a>



<a href="https://msdn.microsoft.com/b0bb2510-44be-4598-96ea-9b8fdcc7f7c6">CM_Locate_DevNode</a>



<a href="https://msdn.microsoft.com/255d828c-5a71-4d53-80ee-b0a0b3e97414">CM_Locate_DevNode_Ex</a>



<a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a>



<a href="https://msdn.microsoft.com/03e6c137-5a7f-443d-878f-5e5c6642dde9">SP_DEVINFO_LIST_DETAIL_DATA</a>



<a href="https://msdn.microsoft.com/3f624882-9ccc-4be1-92aa-8bba9f0022ea">SetupDiGetDeviceInfoListDetail</a>
 

 

