---
UID: NF:rometadataresolution.RoIsApiContractPresent
title: RoIsApiContractPresent (rometadataresolution.h)
ms.date: 02/13/2020
tech.root: WinRT
targetos: Windows
description: Returns true or false to indicate whether the API contract with the specified name and major and minor version number is present.
helpviewer_keywords: ["RoIsApiContractPresent"]
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.header: rometadataresolution.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: WindowsApp.lib
req.dll: WinTypes.dll
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2019 [desktop apps \| UWP apps]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - ext-ms-win-ro-typeresolution-l1-1-1.dll
 - api-ms-win-ro-typeresolution-l1-1-1.dll
 - rometadataresolution.h
api_name:
 - RoIsApiContractPresent
f1_keywords:
 - RoIsApiContractPresent
 - rometadataresolution/RoIsApiContractPresent
dev_langs:
 - c++
---

# RoIsApiContractPresent function


## -description

Returns true or false to indicate whether the API contract with the specified name and major and minor version number is present.

## -parameters

### -param name

Type: <b>PCWSTR</b>

The name of the API contract.

### -param majorVersion

Type: <b>UINT16</b>

The major version number of the API contract.

### -param minorVersion

Type: <b>UINT16</b>

The minor version number of the API contract.

### -param present

Type: <b>BOOL*</b>

True if the specified API contract is present; otherwise, false.

## -returns

Type: <b>HRESULT</b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The specified API contract is valid and is present.
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RO_E_METADATA_NAME_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The input string is not an API contract defined in any examined .winmd file.
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RO_E_METADATA_NAME_IS_NAMESPACE</b></dt>
</dl>
</td>
<td width="60%">
The input string is an existing namespace rather than an API contract name.
</td>
</tr>
</table>

## -remarks

This function was introduced in Windows 10, version 1809 (build 17763).

## -see-also

