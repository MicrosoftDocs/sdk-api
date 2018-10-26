---
UID: NF:mprapi.MprInfoRemoveAll
title: MprInfoRemoveAll function
author: windows-sdk-content
description: The MprInfoRemoveAll function removes all information blocks from the specified header.
old-location: rras\mprinforemoveall.htm
tech.root: rras
ms.assetid: 4afa616f-bf4b-4700-8ca1-9bb679bc30ff
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: MprInfoRemoveAll, MprInfoRemoveAll function [RAS], _mpr_mprinforemoveall, mprapi/MprInfoRemoveAll, rras.mprinforemoveall
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a> to retrieve the error message that corresponds to the returned error code.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a>



<a href="https://msdn.microsoft.com/389002c9-2d24-4b35-ab5b-801fe2091db9">MprInfo Functions and Information Headers</a>



<a href="https://msdn.microsoft.com/2d124541-c954-4031-95cd-68a96c8e0a77">MprInfoBlockRemove</a>
 

 

