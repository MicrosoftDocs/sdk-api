---
UID: NF:cfgmgr32.CM_Add_IDA
tech.root: devinst 
title: CM_Add_IDA
ms.date: 04/12/2021
targetos: Windows
description: The CM_Add_ID function appends a specified device ID (if not already present) to a device instance's hardware ID list or compatible ID list.
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
 - CM_Add_IDA
 - CM_Add_ID
f1_keywords:
 - CM_Add_IDA
 - cfgmgr32/CM_Add_IDA
 - CM_Add_ID
 - cfgmgr32/CM_Add_ID
dev_langs:
 - c++
---

# CM_Add_IDA function

## -description

The <b>CM_Add_ID</b> function appends a specified <a href="/windows-hardware/drivers/install/device-ids">device ID</a> (if not already present) to a <a href="/windows-hardware/drivers/">device instance's</a> <a href="/windows-hardware/drivers/install/hardware-ids">hardware ID</a> list or <a href="/windows-hardware/drivers/install/compatible-ids">compatible ID</a> list.

## -parameters

### -param dnDevInst

Caller-supplied device instance handle that is bound to the local machine.

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

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

The <b>CM_Add_ID</b> function can only be used when <i>dnDevInst</i> represents a root-enumerated device. For other devices, the bus driver reports hardware and compatible IDs when enumerating a child device after receiving <a href="/windows-hardware/drivers/kernel/irp-mn-query-id">IRP_MN_QUERY_ID</a>.

Each appended device ID is considered less compatible than IDs already existing in the specified list. For information about device IDs, hardware IDs, and compatible IDs, see <a href="/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.

Callers of this function must have <b>SeLoadDriverPrivilege</b>. (Privileges are described in the Microsoft Windows SDK documentation.)

For information about using device instance handles that are bound to the local machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_id_exa">CM_Add_ID_Ex</a>  
<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>