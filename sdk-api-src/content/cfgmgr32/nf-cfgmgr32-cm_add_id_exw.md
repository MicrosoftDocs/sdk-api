---
UID: NF:cfgmgr32.CM_Add_ID_ExW
title: CM_Add_ID_ExW function (cfgmgr32.h)
description: The CM_Add_ID_Ex function appends a device ID (if not already present) to a device instance's hardware ID list or compatible ID list, on either the local or a remote machine. (Unicode)
helpviewer_keywords: ["CM_Add_ID_Ex", "CM_Add_ID_Ex function [Device and Driver Installation]", "CM_Add_ID_ExW", "cfgmgr32/CM_Add_ID_Ex", "cfgmgr32/CM_Add_ID_ExW", "cfgmgrfn_0c8f48d0-09e5-46f9-b638-aff20af6abd5.xml", "devinst.cm_add_id_ex"]
old-location: devinst\cm_add_id_ex.htm
tech.root: devinst
ms.assetid: 978d650b-cbd5-4dff-bd51-7419774b8a7f
ms.date: 12/05/2018
ms.keywords: CM_Add_ID_Ex, CM_Add_ID_Ex function [Device and Driver Installation], CM_Add_ID_ExW, cfgmgr32/CM_Add_ID_Ex, cfgmgr32/CM_Add_ID_ExW, cfgmgrfn_0c8f48d0-09e5-46f9-b638-aff20af6abd5.xml, devinst.cm_add_id_ex
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Add_ID_ExW
 - cfgmgr32/CM_Add_ID_ExW
dev_langs:
 - c++
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
---

# CM_Add_ID_ExW function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_idw">CM_Add_ID</a> instead.]

The <b>CM_Add_ID_Ex</b> function appends a <a href="/windows-hardware/drivers/install/device-ids">device ID</a> (if not already present) to a device instance's <a href="/windows-hardware/drivers/install/hardware-ids">hardware ID</a> list or <a href="/windows-hardware/drivers/install/compatible-ids">compatible ID</a> list, on either the local or a remote machine.

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

Each appended device ID is considered less compatible than IDs already existing in the specified list. For information about device IDs, hardware IDs, and compatible IDs, see <a href="/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>. 

Callers of this function must have <b>SeLoadDriverPrivilege</b>. (Privileges are described in the Microsoft Windows SDK documentation.)

For information about using device instance handles that are bound to a local or a remote machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>.

Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_idw">CM_Add_ID</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>
