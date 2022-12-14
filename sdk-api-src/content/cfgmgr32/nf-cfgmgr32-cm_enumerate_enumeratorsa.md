---
UID: NF:cfgmgr32.CM_Enumerate_EnumeratorsA
tech.root: devinst 
title: CM_Enumerate_EnumeratorsA
ms.date: 04/12/2021
targetos: Windows
description: The CM_Enumerate_Enumerators function enumerates the local machine's device enumerators by supplying each enumerator's name. (ANSI)
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
 - CM_Enumerate_EnumeratorsA
 - CM_Enumerate_Enumerators
f1_keywords:
 - CM_Enumerate_EnumeratorsA
 - cfgmgr32/CM_Enumerate_EnumeratorsA
 - CM_Enumerate_Enumerators
 - cfgmgr32/CM_Enumerate_Enumerators
dev_langs:
 - c++
---

# CM_Enumerate_EnumeratorsA function

## -description

The <b>CM_Enumerate_Enumerators</b> function enumerates the local machine's device enumerators by supplying each enumerator's name.

## -parameters

### -param ulEnumIndex [in]

Caller-supplied index into the machine's list of device enumerators. For more information, see the following <b>Remarks</b> section.

### -param Buffer [out]

Address of a buffer to receive an enumerator name. This buffer should be MAX_DEVICE_ID_LEN-sized (or, set <i>Buffer</i> to zero and obtain the actual name length in the location referenced by <i>puLength</i>).

### -param pulLength [in, out]

Caller-supplied address of a location to hold the buffer size. The caller supplies the length of the buffer pointed to by <i>Buffer</i>. The function replaces this value with the actual size of the enumerator's name string. If the caller-supplied buffer length is too small, the function supplies the required buffer size and returns CR_BUFFER_SMALL.

### -param ulFlags [in]

Not used, must be zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

To enumerate the local machine's device enumerators, call <b>CM_Enumerate_Enumerators</b> repeatedly, starting with a <i>ulEnumIndex</i> index value of zero. and incrementing the index value with each subsequent call until the function returns CR_NO_SUCH_VALUE.

After enumerator names have been obtained, the names can be used as input to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista">CM_Get_Device_ID_List</a>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_enumerate_enumerators_exa">CM_Enumerate_Enumerators_Ex</a>
