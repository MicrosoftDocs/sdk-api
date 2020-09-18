---
UID: NF:mprapi.MprInfoDuplicate
title: MprInfoDuplicate function (mprapi.h)
description: The MprInfoDuplicate function duplicates an existing information header.
helpviewer_keywords: ["MprInfoDuplicate","MprInfoDuplicate function [RAS]","_mpr_mprinfoduplicate","mprapi/MprInfoDuplicate","rras.mprinfoduplicate"]
old-location: rras\mprinfoduplicate.htm
tech.root: RRAS
ms.assetid: 446e93a0-8de5-4117-94fe-6f167da1acef
ms.date: 12/05/2018
ms.keywords: MprInfoDuplicate, MprInfoDuplicate function [RAS], _mpr_mprinfoduplicate, mprapi/MprInfoDuplicate, rras.mprinfoduplicate
req.header: mprapi.h
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
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprInfoDuplicate
 - mprapi/MprInfoDuplicate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprInfoDuplicate
---

# MprInfoDuplicate function


## -description

The 
<b>MprInfoDuplicate</b> function duplicates an existing information header.

## -parameters

### -param lpHeader [in]

Pointer to the information header to duplicate.

### -param lplpNewHeader [out]

Pointer to a pointer variable. On successful return, this variable points to the new (duplicate) information header.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lplpNewHeader</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The requested memory allocation could not be completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
The call failed. Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the error message that corresponds to the returned error code.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/RRAS/understanding-mprinfo-functions-and-information-headers">MprInfo Functions and Information Headers</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprinfocreate">MprInfoCreate</a>