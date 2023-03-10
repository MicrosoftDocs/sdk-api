---
UID: NC:routprot.PGET_GLOBAL_INFO
title: PGET_GLOBAL_INFO (routprot.h)
description: The GetGlobalInfo function retrieves global (as opposed to interface-specific) configuration information kept by the routing protocol.
helpviewer_keywords: ["GetGlobalInfo","GetGlobalInfo callback function [RAS]","PGET_GLOBAL_INFO","PGET_GLOBAL_INFO callback","_mpr_getglobalinfo","routprot/GetGlobalInfo","rras.getglobalinfo"]
old-location: rras\getglobalinfo.htm
tech.root: RRAS
ms.assetid: 89d4ca42-8f78-40bd-96f0-ad10181cb2d4
ms.date: 12/05/2018
ms.keywords: GetGlobalInfo, GetGlobalInfo callback function [RAS], PGET_GLOBAL_INFO, PGET_GLOBAL_INFO callback, _mpr_getglobalinfo, routprot/GetGlobalInfo, rras.getglobalinfo
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
 - PGET_GLOBAL_INFO
 - routprot/PGET_GLOBAL_INFO
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
 - GetGlobalInfo
---

# PGET_GLOBAL_INFO callback function


## -description

The 
<b>GetGlobalInfo</b> function retrieves global (as opposed to interface-specific) configuration information kept by the routing protocol.

## -parameters

### -param GlobalInfo [in]

Pointer to a buffer to receive the protocol-defined global configuration information. The format of this information is specific to the routing protocol.

### -param BufferSize

### -param StructureVersion

### -param StructureSize

### -param StructureCount

#### - GlobalInfoSize [in, out]

Pointer to a <b>DWORD</b> variable. 




On input this variable specifies the size, in bytes, of the buffer pointed to by the <i>GlobalInfo</i> parameter.

On output this variable receives the size, in bytes, of the data placed in the output buffer. If the initial size was not large enough, the variable contains the size required to hold all of the output data.

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
The routing protocol could not retrieve the global information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of the output buffer provided is not large enough to hold the requested information. The required size is returned in the <b>DWORD</b> variable pointed to by <i>OutputDataSize</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>GlobalInfoSize</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/RRAS/routing-protocol-interface-functions">Routing Protocol Interface Functions</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pset_global_info">SetGlobalInfo</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pset_interface_info">SetInterfaceInfo</a>