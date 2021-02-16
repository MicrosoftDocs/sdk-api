---
UID: NC:routprot.PMIB_GET_TRAP_INFO
title: PMIB_GET_TRAP_INFO (routprot.h)
description: The MibGetTrapInfo function queries the module that set a trap event for more information about the trap.
helpviewer_keywords: ["MibGetTrapInfo","MibGetTrapInfo callback function [RAS]","PMIB_GET_TRAP_INFO","PMIB_GET_TRAP_INFO callback","_mpr_mibgettrapinfo","routprot/MibGetTrapInfo","rras.mibgettrapinfo"]
old-location: rras\mibgettrapinfo.htm
tech.root: RRAS
ms.assetid: 2eb77b83-27bb-414b-8fbf-519d5e0cb08a
ms.date: 12/05/2018
ms.keywords: MibGetTrapInfo, MibGetTrapInfo callback function [RAS], PMIB_GET_TRAP_INFO, PMIB_GET_TRAP_INFO callback, _mpr_mibgettrapinfo, routprot/MibGetTrapInfo, rras.mibgettrapinfo
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
 - PMIB_GET_TRAP_INFO
 - routprot/PMIB_GET_TRAP_INFO
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
 - MibGetTrapInfo
---

# PMIB_GET_TRAP_INFO callback function


## -description

The <b>MibGetTrapInfo</b> function queries the module that set a trap event for more information about the trap.

The <a href="/windows/desktop/api/routprot/ns-routprot-mpr50_routing_characteristics">PMIB_GET_TRAP_INFO</a> type defines a pointer to this callback function. <i>MibGetTrapInfo</i> is a placeholder for the application-defined function name.

## -parameters

### -param InputDataSize [in]

Specifies a <b>ULONG</b> variable that specifies the size in bytes of the data pointed to by <i>InputData</i>.

### -param InputData [in]

Pointer to the input data.

### -param OutputDataSize [out]

Pointer to a <b>ULONG</b> variable that receives the size in bytes of the data pointed to by * <i>OutputData</i>.

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

<a href="/windows/desktop/api/routprot/nc-routprot-pmib_set_trap_info">MibSetTrapInfo</a>