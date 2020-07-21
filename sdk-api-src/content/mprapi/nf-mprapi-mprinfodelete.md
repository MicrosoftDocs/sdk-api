---
UID: NF:mprapi.MprInfoDelete
title: MprInfoDelete function (mprapi.h)
description: The MprInfoDelete function deletes an information header created using MprInfoCreate, or retrieved by MprInfoBlockAdd, MprInfoBlockRemove, or MprInfoBlockSet.
helpviewer_keywords: ["MprInfoDelete","MprInfoDelete function [RAS]","_mpr_mprinfodelete","mprapi/MprInfoDelete","rras.mprinfodelete"]
old-location: rras\mprinfodelete.htm
tech.root: RRAS
ms.assetid: c81b92c2-a977-40e0-b971-e4e70e1a1371
ms.date: 12/05/2018
ms.keywords: MprInfoDelete, MprInfoDelete function [RAS], _mpr_mprinfodelete, mprapi/MprInfoDelete, rras.mprinfodelete
f1_keywords:
- mprapi/MprInfoDelete
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
- MprInfoDelete
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprInfoDelete function


## -description


The 
<b>MprInfoDelete</b> function deletes an information header created using 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mprinfocreate">MprInfoCreate</a>, or retrieved by 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockadd">MprInfoBlockAdd</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockremove">MprInfoBlockRemove</a>, or 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockset">MprInfoBlockSet</a>.


## -parameters




### -param lpHeader [in]

Pointer to the header to be deallocated.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails the return value is one of the following values.

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
The <i>lpHeader</i> parameter is <b>NULL</b>.

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
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the error message that corresponds to the returned error code.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockadd">MprInfoBlockAdd</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockremove">MprInfoBlockRemove</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockset">MprInfoBlockSet</a>
 

 

