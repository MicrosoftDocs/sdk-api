---
UID: NC:routprot.PMIB_SET_TRAP_INFO
title: PMIB_SET_TRAP_INFO (routprot.h)
description: The MibSetTrapInfo function passes in a handle to an event which is signaled whenever a TRAP needs to be issued.
helpviewer_keywords: ["MibSetTrapInfo","MibSetTrapInfo callback function [RAS]","PMIB_SET_TRAP_INFO","PMIB_SET_TRAP_INFO callback","_mpr_mibsettrapinfo","routprot/MibSetTrapInfo","rras.mibsettrapinfo"]
old-location: rras\mibsettrapinfo.htm
tech.root: RRAS
ms.assetid: 28056113-82a5-4493-ba49-509db3606fa0
ms.date: 12/05/2018
ms.keywords: MibSetTrapInfo, MibSetTrapInfo callback function [RAS], PMIB_SET_TRAP_INFO, PMIB_SET_TRAP_INFO callback, _mpr_mibsettrapinfo, routprot/MibSetTrapInfo, rras.mibsettrapinfo
req.header: routprot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PMIB_SET_TRAP_INFO
 - routprot/PMIB_SET_TRAP_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Routprot.h
api_name:
 - MibSetTrapInfo
---

# PMIB_SET_TRAP_INFO callback function


## -description

The 
<i>MibSetTrapInfo</i> function passes in a handle to an event which is signaled whenever a TRAP needs to be issued.

The <a href="/windows/desktop/api/routprot/ns-routprot-mpr50_routing_characteristics">PMIP_SET_TRAP_INFO</a> type defines a pointer to this callback function. <i>MibSetTrapInfo</i> is a placeholder for the application-defined function name.

## -parameters

### -param Event [in]

Handle to an event that is signaled when a TRAP needs to be issued.

### -param InputDataSize [in]

Specifies a <b>ULONG</b> variable that contains the size in bytes of the data pointed to by <i>InputData</i>.

### -param InputData [in]

Pointer to the input data.

### -param OutputDataSize [out]

Pointer to a <b>ULONG</b> variable that specifies the size in bytes of the data pointed to by * <i>OutputData</i>.

### -param OutputData [out]

Receives the address of a pointer to the output data.

## -returns

If the functions succeeds, the return value is NO_ERROR

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient resources to complete the operation.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/routprot/nc-routprot-pmib_get_trap_info">MibGetTrapInfo</a>