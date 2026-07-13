---
UID: NF:cfgmgr32.CM_Enumerate_Enumerators_ExW
title: CM_Enumerate_Enumerators_ExW function (cfgmgr32.h)
description: The CM_Enumerate_Enumerators_Ex function enumerates a local or a remote machine's device enumerators, by supplying each enumerator's name. (Unicode)
helpviewer_keywords: ["CM_Enumerate_Enumerators_Ex", "CM_Enumerate_Enumerators_Ex function [Device and Driver Installation]", "CM_Enumerate_Enumerators_ExW", "cfgmgr32/CM_Enumerate_Enumerators_Ex", "cfgmgr32/CM_Enumerate_Enumerators_ExW", "cfgmgrfn_56f59835-4383-4d6f-aaa5-e7e1cb4a3b56.xml", "devinst.cm_enumerate_enumerators_ex"]
old-location: devinst\cm_enumerate_enumerators_ex.htm
tech.root: devinst
ms.assetid: 9d44b1be-96b1-493a-94b7-a6bd883fd570
ms.date: 12/05/2018
ms.keywords: CM_Enumerate_Enumerators_Ex, CM_Enumerate_Enumerators_Ex function [Device and Driver Installation], CM_Enumerate_Enumerators_ExW, cfgmgr32/CM_Enumerate_Enumerators_Ex, cfgmgr32/CM_Enumerate_Enumerators_ExW, cfgmgrfn_56f59835-4383-4d6f-aaa5-e7e1cb4a3b56.xml, devinst.cm_enumerate_enumerators_ex
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Enumerate_Enumerators_ExW (Unicode)
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
 - CM_Enumerate_Enumerators_ExW
 - cfgmgr32/CM_Enumerate_Enumerators_ExW
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
 - CM_Enumerate_Enumerators_Ex
 - CM_Enumerate_Enumerators_ExW
---

# CM_Enumerate_Enumerators_ExW function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw">CM_Enumerate_Enumerators</a> instead.]

The <b>CM_Enumerate_Enumerators_Ex</b> function enumerates a local or a remote machine's device enumerators, by supplying each enumerator's name.

## -parameters

### -param ulEnumIndex [in]

Caller-supplied index into the machine's list of device enumerators. For more information, see the following <b>Remarks</b> section.

### -param Buffer [out]

Address of a buffer to receive an enumerator name. This buffer should be MAX_DEVICE_ID_LEN-sized (or, set <i>Buffer</i> to zero and obtain the actual name length in the location referenced by <b>puLength</b>).

### -param pulLength [in, out]

Caller-supplied address of a location to hold the buffer size. The caller supplies the length of the buffer pointed to by <i>Buffer</i>. The function replaces this value with the actual size of the enumerator's name string. If the caller-supplied buffer length is too small, the function supplies the required buffer size and returns CR_BUFFER_SMALL.

### -param ulFlags [in]

Not used, must be zero.

### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

To enumerate the local or a remote machine's device enumerators, call <b>CM_Enumerate_Enumerators_Ex</b> repeatedly, starting with a <i>ulEnumIndex</i> index value of zero, and incrementing the index value with each subsequent call until the function returns CR_NO_SUCH_VALUE.

After enumerator names have been obtained, the names can be used as input to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista">CM_Get_Device_ID_List</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw">CM_Enumerate_Enumerators</a>
