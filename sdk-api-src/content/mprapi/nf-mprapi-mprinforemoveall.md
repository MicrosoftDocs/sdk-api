---
UID: NF:mprapi.MprInfoRemoveAll
title: MprInfoRemoveAll function (mprapi.h)
description: The MprInfoRemoveAll function removes all information blocks from the specified header.
old-location: rras\mprinforemoveall.htm
tech.root: RRAS
ms.assetid: 4afa616f-bf4b-4700-8ca1-9bb679bc30ff
ms.date: 12/05/2018
ms.keywords: MprInfoRemoveAll, MprInfoRemoveAll function [RAS], _mpr_mprinforemoveall, mprapi/MprInfoRemoveAll, rras.mprinforemoveall
ms.topic: function
f1_keywords:
- mprapi/MprInfoRemoveAll
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Mprapi.dll
api_name:
- MprInfoRemoveAll
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprInfoRemoveAll function


## -description


The 
<b>MprInfoRemoveAll</b> function removes all information blocks from the specified header.


## -parameters




### -param lpHeader [in]

Pointer to the information header from which to remove all information blocks.


### -param lplpNewHeader [out]

Pointer to a pointer variable. On successful return, this variable points to the information header with all information blocks removed.


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
Either the <i>lpHeader</i> parameter is <b>NULL</b> or the <i>lplpNewHeader</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the error message that corresponds to the returned error code.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/understanding-mprinfo-functions-and-information-headers">MprInfo Functions and Information Headers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockremove">MprInfoBlockRemove</a>
 

 

