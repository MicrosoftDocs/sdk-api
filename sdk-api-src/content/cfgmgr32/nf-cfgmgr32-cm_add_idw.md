---
UID: NF:cfgmgr32.CM_Add_IDW
title: CM_Add_IDW function (cfgmgr32.h)
description: The CM_Add_ID function appends a specified device ID (if not already present) to a device instance's hardware ID list or compatible ID list.
helpviewer_keywords: ["CM_Add_ID", "CM_Add_ID function [Device and Driver Installation]", "CM_Add_IDW", "cfgmgr32/CM_Add_ID", "cfgmgr32/CM_Add_IDW", "cfgmgrfn_70bf6b8b-4ab4-47aa-b24e-873af6a3712c.xml", "devinst.cm_add_id"]
old-location: devinst\cm_add_id.htm
tech.root: devinst
ms.assetid: 0a2da246-7803-45cb-baee-351726dbcf15
ms.date: 12/05/2018
ms.keywords: CM_Add_ID, CM_Add_ID function [Device and Driver Installation], CM_Add_IDW, cfgmgr32/CM_Add_ID, cfgmgr32/CM_Add_IDW, cfgmgrfn_70bf6b8b-4ab4-47aa-b24e-873af6a3712c.xml, devinst.cm_add_id
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Add_IDW (Unicode)
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
 - CM_Add_IDW
 - cfgmgr32/CM_Add_IDW
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
 - CM_Add_ID
 - CM_Add_IDW
---

# CM_Add_IDW function


## -description

The <b>CM_Add_ID</b> function appends a specified <a href="/windows-hardware/drivers/install/device-ids">device ID</a> (if not already present) to a <a href="/windows-hardware/drivers/">device instance's</a> <a href="/windows-hardware/drivers/install/hardware-ids">hardware ID</a> list or <a href="/windows-hardware/drivers/install/compatible-ids">compatible ID</a> list.

## -parameters

### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the local machine.

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

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

The <b>CM_Add_ID</b> function can only be used when <i>dnDevInst</i> represents a root-enumerated device.     For other devices, the bus driver reports hardware and compatible IDs when enumerating a child device after receiving <a href="/windows-hardware/drivers/kernel/irp-mn-query-id">IRP_MN_QUERY_ID</a>.

Each appended device ID is considered less compatible than IDs already existing in the specified list. For information about device IDs, hardware IDs, and compatible IDs, see <a href="/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>. 

Callers of this function must have <b>SeLoadDriverPrivilege</b>. (Privileges are described in the Microsoft Windows SDK documentation.)

For information about using device instance handles that are bound to the local machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_id_exw">CM_Add_ID_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>
