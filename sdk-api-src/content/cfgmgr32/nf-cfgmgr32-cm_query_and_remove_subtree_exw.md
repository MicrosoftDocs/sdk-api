---
UID: NF:cfgmgr32.CM_Query_And_Remove_SubTree_ExW
title: CM_Query_And_Remove_SubTree_ExW function
author: windows-sdk-content
description: The CM_Query_And_Remove_SubTree_Ex function checks whether a device instance and its children can be removed and, if so, it removes them.
old-location: devinst\cm_query_and_remove_subtree_ex.htm
old-project: devinst
ms.assetid: c8a3af37-0886-4187-9cdb-49616bcb04a9
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: CM_Query_And_Remove_SubTree_Ex, CM_Query_And_Remove_SubTree_Ex function [Device and Driver Installation], CM_Query_And_Remove_SubTree_ExW, cfgmgr32/CM_Query_And_Remove_SubTree_Ex, cfgmgr32/CM_Query_And_Remove_SubTree_ExW, cfgmgrfn_69fa61ff-b77c-41d7-a263-facf56883977.xml, devinst.cm_query_and_remove_subtree_ex
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
req.unicode-ansi: CM_Query_And_Remove_SubTree_ExW (Unicode)
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
 - LibDef
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
api_name:
 - CM_Query_And_Remove_SubTree_Ex
 - CM_Query_And_Remove_SubTree_ExW
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
---

# CM_Query_And_Remove_SubTree_ExW function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/library/windows/hardware/ff539722">CM_Query_And_Remove_SubTree</a> instead.]

The <b>CM_Query_And_Remove_SubTree_Ex</b> function checks whether a device instance and its children can be removed and, if so, it removes them.


## -parameters




### -param dnAncestor [in]

Caller-supplied device instance handle to the device at the root of the subtree to be removed. This device instance handle is bound to the machine handle supplied by <i>hMachine</i>. 


### -param pVetoType [out, optional]

(<i>Optional</i>.) If not <b>NULL</b>, this points to a location that, if the removal request fails, receives a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549728">PNP_VETO_TYPE</a>-typed value indicating the reason for the failure.


### -param pszVetoName [out, optional]

(<i>Optional</i>.) If not <b>NULL</b>, this is a caller-supplied pointer to a string buffer that receives a text string. The type of information this string provides is dependent on the value received by <i>pVetoType</i>. For information about these strings, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff549728">PNP_VETO_TYPE</a>.


### -param ulNameLength [in]

(<i>Optional</i>.) Caller-supplied value representing the length (number of characters) of the string buffer supplied by <i>pszVetoName</i>. This should be set to MAX_PATH.


### -param ulFlags [in]

A bitwise OR of the caller-supplied flag constants that are described in the <b>Remarks</b> section. 


### -param hMachine [in, optional]

Caller-supplied machine handle to which the caller-supplied device instance handle is bound.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



The purpose of the <b>CM_Query_And_Remove_SubTree_Ex</b> function is to allow an application to prepare a device for safe removal from a remote machine. Use this function to remove devices only if a driver has not set the <b>SurpriseRemovalOK</b> member of <a href="https://msdn.microsoft.com/library/windows/hardware/ff543095">DEVICE_CAPABILITIES</a>. If a driver has set <b>SurpriseRemovalOK</b>, the application should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff539807">CM_Request_Device_Eject_Ex</a> instead of <b>CM_Query_And_Remove_SubTree_Ex</b>.

<b>CM_Query_And_Remove_SubTree_Ex</b> supports setting the flags parameter <i>ulFlags</i> with one of the following two flags; these flags apply only if Windows or an installer vetoes the removal of a device: 



Beginning with Windows XP, <b>CM_Query_And_Remove_SubTree_Ex</b> also supports setting the following additional flag; this flag applies only if the function successfully removes the device instance: 



<a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">Device installation applications</a> that do not require the low-level operation of <b>CM_Query_And_Remove_SubTree_Ex</b> should use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff543712">DIF_PROPERTYCHANGE</a> request to disable a device instead of using <b>CM_Query_And_Remove_SubTree_Ex</b> to remove a device. The DIF_PROPERTYCHANGE request can be used to enable, disable, restart, stop, or change the properties of a device. 

Callers of this function must have <b>SeLoadDriverPrivilege</b>. (Privileges are described in the Microsoft Windows SDK documentation.)

For information about using device instance handles that are bound to a local or a remote machine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff538076">CM_Get_Child_Ex</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538076">CM_Get_Child_Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539722">CM_Query_And_Remove_SubTree</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539763">CM_Reenumerate_DevNode</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539807">CM_Request_Device_Eject_Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539825">CM_Setup_DevNode</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543712">DIF_PROPERTYCHANGE</a>
 

 

