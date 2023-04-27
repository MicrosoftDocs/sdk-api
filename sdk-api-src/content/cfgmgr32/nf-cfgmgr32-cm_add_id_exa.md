---
UID: NF:cfgmgr32.CM_Add_ID_ExA
tech.root: devinst
title: CM_Add_ID_ExA
ms.date: 04/12/2021
targetos: Windows
description: The CM_Add_ID_Ex function appends a device ID (if not already present) to a device instance's hardware ID list or compatible ID list, on either the local or a remote machine. (ANSI)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: cfgmgr32.h
req.idl: 
req.include-header: Cfgmgr32.h 
req.irql: 
req.kmdf-ver: 
req.lib: Cfgmgr32.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.target-type: Desktop
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
api_name:
 - CM_Add_ID_ExA
 - CM_Add_ID_Ex
f1_keywords:
 - CM_Add_ID_ExA
 - cfgmgr32/CM_Add_ID_ExA
 - CM_Add_ID_Ex
 - cfgmgr32/CM_Add_ID_Ex
dev_langs:
 - c++
---

# CM_Add_ID_ExA function

## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated. Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_ida">CM_Add_ID</a> instead.]

The <b>CM_Add_ID_Ex</b> function appends a <a href="/windows-hardware/drivers/install/device-ids">device ID</a> (if not already present) to a device instance's <a href="/windows-hardware/drivers/install/hardware-ids">hardware ID</a> list or <a href="/windows-hardware/drivers/install/compatible-ids">compatible ID</a> list, on either the local or a remote machine.

## -parameters

### -param dnDevInst

Caller-supplied device instance handle that is bound to the machine handle supplied by <i>hMachine</i>.

### -param pszID

Caller-supplied pointer to a NULL-terminated device ID string.

### -param ulFlags

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

### -param hMachine

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

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_ida">CM_Add_ID</a>  
<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>
