---
UID: NF:mprapi.MprInfoCreate
title: MprInfoCreate function
author: windows-sdk-content
description: The MprInfoCreate function creates a new information header.
old-location: rras\mprinfocreate.htm
tech.root: rras
ms.assetid: c48fc24f-8cf6-45c0-8ce1-841896648ba7
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: MprInfoCreate, MprInfoCreate function [RAS], _mpr_mprinfocreate, mprapi/MprInfoCreate, rras.mprinfocreate
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
 - MprInfoCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a> to retrieve the error message that corresponds to the returned error code.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a>



<a href="https://msdn.microsoft.com/389002c9-2d24-4b35-ab5b-801fe2091db9">MprInfo Functions and Information Headers</a>
 

 

