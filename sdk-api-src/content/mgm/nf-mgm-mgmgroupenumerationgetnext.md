---
UID: NF:mgm.MgmGroupEnumerationGetNext
title: MgmGroupEnumerationGetNext function (mgm.h)
description: The MgmGroupEnumerationGetNext function retrieves the next set of group entries. The information that is returned by this function is a list of groups joined and the sources requested, if any.
helpviewer_keywords: ["MgmGroupEnumerationGetNext","MgmGroupEnumerationGetNext function [RAS]","_mpr_mgmgroupenumerationgetnext","mgm/MgmGroupEnumerationGetNext","rras.mgmgroupenumerationgetnext"]
old-location: rras\mgmgroupenumerationgetnext.htm
tech.root: RRAS
ms.assetid: a5e659e9-b566-490b-831b-96f9de822ebf
ms.date: 12/05/2018
ms.keywords: MgmGroupEnumerationGetNext, MgmGroupEnumerationGetNext function [RAS], _mpr_mgmgroupenumerationgetnext, mgm/MgmGroupEnumerationGetNext, rras.mgmgroupenumerationgetnext
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
 - MgmGroupEnumerationGetNext
 - mgm/MgmGroupEnumerationGetNext
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
 - MgmGroupEnumerationGetNext
---

# MgmGroupEnumerationGetNext function


## -description

The 
<b>MgmGroupEnumerationGetNext</b> function retrieves the next set of group entries. The information that is returned by this function is a list of groups joined and the sources requested, if any.

The groups are not returned in any particular order.

## -parameters

### -param hEnum [in]

Handle to the enumeration that was obtained from a previous call to 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationstart">MgmGroupEnumerationStart</a>.

### -param pdwBufferSize [in, out]

On input, <i>pdwBufferSize</i> is a pointer to a <b>DWORD</b>-sized memory location that contains the size, in bytes, of the buffer pointed to by <i>pbBuffer</i>. 




On output, if the return value is ERROR_INSUFFICIENT_BUFFER, <i>pdwBufferSize</i> receives the minimum size that the buffer pointed to by <i>pbBuffer</i> must be to hold a group entry; otherwise the value of <i>pdwBufferSize</i> remains unchanged.

### -param pbBuffer [in, out]

On input, the client must supply a pointer to a buffer. 




On output, <i>pbBuffer</i> contains one or more group entries. Each group entry is a 
<a href="/windows/desktop/api/mgm/ns-mgm-source_group_entry">SOURCE_GROUP_ENTRY</a> structure.

### -param pdwNumEntries [in, out]

On input, the client must supply a pointer to a <b>DWORD</b> value. 




On output, <i>pdwNumEntries</i> receives the number of groups in <i>pbBuffer</i>.

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
The specified buffer is too small to hold even one group. The client should check the value of <i>pdwBufferSize</i> for the minimum buffer size required to retrieve one group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Invalid handle to an enumeration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More groups are available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
No more groups are available. Zero or more groups were returned; check the value of <i>pdwNumEntries</i> to verify how many groups were returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to complete this operation.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationend">MgmGroupEnumerationEnd</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationstart">MgmGroupEnumerationStart</a>



<a href="/windows/desktop/api/mgm/ns-mgm-source_group_entry">SOURCE_GROUP_ENTRY</a>