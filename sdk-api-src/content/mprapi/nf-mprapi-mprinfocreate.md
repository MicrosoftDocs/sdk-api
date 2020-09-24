---
UID: NF:mprapi.MprInfoCreate
title: MprInfoCreate function (mprapi.h)
description: The MprInfoCreate function creates a new information header.
helpviewer_keywords: ["MprInfoCreate","MprInfoCreate function [RAS]","_mpr_mprinfocreate","mprapi/MprInfoCreate","rras.mprinfocreate"]
old-location: rras\mprinfocreate.htm
tech.root: RRAS
ms.assetid: c48fc24f-8cf6-45c0-8ce1-841896648ba7
ms.date: 12/05/2018
ms.keywords: MprInfoCreate, MprInfoCreate function [RAS], _mpr_mprinfocreate, mprapi/MprInfoCreate, rras.mprinfocreate
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
 - MprInfoCreate
 - mprapi/MprInfoCreate
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
 - MprInfoCreate
---

# MprInfoCreate function


## -description

The 
<b>MprInfoCreate</b> function creates a new information header.

## -parameters

### -param dwVersion [in]

Specifies the version of the information header structure to be created. The only value currently supported is RTR_INFO_BLOCK_VERSION, as declared in Mprapi.h.

### -param lplpNewHeader [out]

Pointer to the allocated and initialized header.

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