---
UID: NF:mgm.MgmGetMfe
title: MgmGetMfe function (mgm.h)
description: The MgmGetMfe function retrieves a specific MFE.
helpviewer_keywords: ["MgmGetMfe","MgmGetMfe function [RAS]","_mpr_mgmgetmfe","mgm/MgmGetMfe","rras.mgmgetmfe"]
old-location: rras\mgmgetmfe.htm
tech.root: RRAS
ms.assetid: 15b1b096-9044-4983-9039-e7a13c2cca25
ms.date: 12/05/2018
ms.keywords: MgmGetMfe, MgmGetMfe function [RAS], _mpr_mgmgetmfe, mgm/MgmGetMfe, rras.mgmgetmfe
req.header: mgm.h
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
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MgmGetMfe
 - mgm/MgmGetMfe
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - MgmGetMfe
---

# MgmGetMfe function


## -description

The 
<b>MgmGetMfe</b> function retrieves a specific MFE.

## -parameters

### -param pimm [in]

Pointer to a 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe">MIB_IPMCAST_MFE</a> structure that specifies the MFE to retrieve. The information to be returned is indicated by the <b>dwSource</b> and <b>dwGroup</b> members of the 
<b>MIB_IPMCAST_MFE</b> structure.

### -param pdwBufferSize [in, out]

On input, <i>pdwBufferSize</i> is a pointer to a <b>DWORD</b>-sized memory location that contains the size, in bytes, of the buffer pointed to by <i>pbBuffer</i>. 




On output, if the return value is ERROR_INSUFFICIENT_BUFFER, <i>pdwBufferSize</i> receives the minimum size the buffer pointed to by <i>pbBuffer</i> must be to hold the MFE; otherwise the value of <i>pdwBufferSize</i> remains unchanged.

### -param pbBuffer [in, out]

On input, the client must supply a pointer to a buffer. 




On output, <i>pbBuffer</i> contains the specified MFE. The MFE is a 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe">MIB_IPMCAST_MFE</a> structure.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Could not complete the call to this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The specified buffer is too small to hold the MFE. The client should check the value of <i>pdwBufferSize</i> for the minimum buffer size required to retrieve the MFE.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified MFE was not found.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe">MIB_IPMCAST_MFE</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmgetfirstmfe">MgmGetFirstMfe</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmgetnextmfe">MgmGetNextMfe</a>