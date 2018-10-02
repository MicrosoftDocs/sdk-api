---
UID: NF:cfgmgr32.CM_Add_ID_ExW
title: CM_Add_ID_ExW function
author: windows-sdk-content
description: The CM_Add_ID_Ex function appends a device ID (if not already present) to a device instance's hardware ID list or compatible ID list, on either the local or a remote machine.
old-location: devinst\cm_add_id_ex.htm
tech.root: devinst
ms.assetid: 978d650b-cbd5-4dff-bd51-7419774b8a7f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CM_Add_ID_Ex, CM_Add_ID_Ex function [Device and Driver Installation], CM_Add_ID_ExW, cfgmgr32/CM_Add_ID_Ex, cfgmgr32/CM_Add_ID_ExW, cfgmgrfn_0c8f48d0-09e5-46f9-b638-aff20af6abd5.xml, devinst.cm_add_id_ex
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
req.unicode-ansi: CM_Add_ID_ExW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
api_name:
 - CM_Add_ID_Ex
 - CM_Add_ID_ExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Add_ID_ExW function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/0a2da246-7803-45cb-baee-351726dbcf15">CM_Add_ID</a> instead.]

The <b>CM_Add_ID_Ex</b> function appends a <a href="devinst.device_ids">device ID</a> (if not already present) to a device instance's <a href="devinst.hardware_ids">hardware ID</a> list or <a href="devinst.compatible_ids">compatible ID</a> list, on either the local or a remote machine.


## -parameters




### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the machine handle supplied by 

<i>hMachine</i>

.


### -param pszID [in]

Caller-supplied pointer to a NULL-terminated device ID string. 


### -param ulFlags [in]

Caller-supplied flag constant that specifies the list onto which the supplied device ID should be appended. The following flag constants are valid.

<table>
<tr>
<th>Flag Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>
CM_ADD_ID_COMPATIBLE

</td>
<td>
The specified device ID should be appended to the specific device instance's compatible ID list.

</td>
</tr>
<tr>
<td>
CM_ADD_ID_HARDWARE

</td>
<td>
The specified device ID should be appended to the specific device instance's hardware ID list.

</td>
</tr>
</table>
 


### -param hMachine [in, optional]

Caller-supplied machine handle to which the caller-supplied device instance handle is bound.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



Each appended device ID is considered less compatible than IDs already existing in the specified list. For information about device IDs, hardware IDs, and compatible IDs, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>. 

Callers of this function must have <b>SeLoadDriverPrivilege</b>. (Privileges are described in the Microsoft Windows SDK documentation.)

For information about using device instance handles that are bound to a local or a remote machine, see <a href="https://msdn.microsoft.com/bcd46252-6f87-4d49-a24c-81789b0148d9">CM_Get_Child_Ex</a>.

Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/0a2da246-7803-45cb-baee-351726dbcf15">CM_Add_ID</a>



<a href="https://msdn.microsoft.com/bcd46252-6f87-4d49-a24c-81789b0148d9">CM_Get_Child_Ex</a>
 

 

