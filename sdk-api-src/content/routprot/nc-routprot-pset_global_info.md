---
UID: NC:routprot.PSET_GLOBAL_INFO
title: PSET_GLOBAL_INFO (routprot.h)
description: The SetGlobalInfo function sets the global (as opposed to interface-specific) configuration information kept by the routing protocol. The format of this information is specific to the routing protocol.
helpviewer_keywords: ["PSET_GLOBAL_INFO","PSET_GLOBAL_INFO callback","PSET_GLOBAL_INFO callback function [RAS]","SetGlobalInfo","_mpr_setglobalinfo","routprot/PSET_GLOBAL_INFO","rras.setglobalinfo"]
old-location: rras\setglobalinfo.htm
tech.root: RRAS
ms.assetid: fd977a71-bfa7-40e4-9afc-4824989f857f
ms.date: 12/05/2018
ms.keywords: PSET_GLOBAL_INFO, PSET_GLOBAL_INFO callback, PSET_GLOBAL_INFO callback function [RAS], SetGlobalInfo, _mpr_setglobalinfo, routprot/PSET_GLOBAL_INFO, rras.setglobalinfo
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
 - PSET_GLOBAL_INFO
 - routprot/PSET_GLOBAL_INFO
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
 - PSET_GLOBAL_INFO
---

# PSET_GLOBAL_INFO callback function


## -description

The 
<b>SetGlobalInfo</b> function sets the global (as opposed to interface-specific) configuration information kept by the routing protocol. The format of this information is specific to the routing protocol.

## -parameters

### -param GlobalInfo [in]

Pointer to a buffer that specifies the protocol-defined global configuration information.

### -param StructureVersion

### -param StructureSize

### -param StructureCount

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The routing protocol could not set the configuration information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>GlobalInfo</i> parameter is <b>NULL</b>, or one of the parameters in the configuration information is invalid.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/routprot/nc-routprot-pget_global_info">GetGlobalInfo</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pget_interface_info">GetInterfaceInfo</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-functions">Routing Protocol Interface Functions</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>