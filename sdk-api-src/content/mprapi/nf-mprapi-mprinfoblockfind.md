---
UID: NF:mprapi.MprInfoBlockFind
title: MprInfoBlockFind function (mprapi.h)
author: windows-sdk-content
description: The MprInfoBlockFind function locates a specified block in an information header, and retrieves information about the block.
old-location: rras\mprinfoblockfind.htm
tech.root: RRAS
ms.assetid: fd9a048b-03fb-4fe9-9f72-df07b35dd804
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MprInfoBlockFind, MprInfoBlockFind function [RAS], _mpr_mprinfoblockfind, mprapi/MprInfoBlockFind, rras.mprinfoblockfind
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
 - MprInfoBlockFind
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprInfoBlockFind function


## -description


The 
<b>MprInfoBlockFind</b> function locates a specified block in an information header, and retrieves information about the block.


## -parameters




### -param lpHeader [in]

Specifies the header in which to locate the block.


### -param dwInfoType [in]

Specifies the type of block to locate. The types available depend on the transport: 
<a href="https://msdn.microsoft.com/911c61d4-e500-48c6-8861-39dbc09ab4e7">IP</a> or 
<a href="https://msdn.microsoft.com/6cbc8415-f5ba-4f84-a23f-dd4f4a54d118">IPX</a>.


### -param lpdwItemSize [out]

Pointer to a <b>DWORD</b> variable that receives the size of each item in the located block's data. This parameter is optional. If this parameter is <b>NULL</b>, the item size is not returned.


### -param lpdwItemCount [out]

Pointer to a <b>DWORD</b> variable that receives the number of items of size <i>dwItemSize</i> contained in the block's data. This parameter is optional. If this parameter is <b>NULL</b>, the item count is not  returned.


### -param lplpItemData [out]

Pointer to a pointer that, on successful return, points to the data for the located block. This parameter is optional. If this parameter is <b>NULL</b>, the data is  not  returned.


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
The <i>lpInfoHeader</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No block of type <i>dwInfoType</i> exists in the header.

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
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a>



<a href="https://msdn.microsoft.com/389002c9-2d24-4b35-ab5b-801fe2091db9">MprInfo Functions and Information Headers</a>
 

 

