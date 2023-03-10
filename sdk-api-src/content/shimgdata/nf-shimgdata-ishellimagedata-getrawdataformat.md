---
UID: NF:shimgdata.IShellImageData.GetRawDataFormat
title: IShellImageData::GetRawDataFormat (shimgdata.h)
description: Retrieves a GUID that identifies the format of the image.
helpviewer_keywords: ["GetRawDataFormat","GetRawDataFormat method [Windows Shell]","GetRawDataFormat method [Windows Shell]","IShellImageData interface","IShellImageData interface [Windows Shell]","GetRawDataFormat method","IShellImageData.GetRawDataFormat","IShellImageData::GetRawDataFormat","_shell_IShellImageData_GetRawDataFormat","shell.IShellImageData_GetRawDataFormat","shimgdata/IShellImageData::GetRawDataFormat"]
old-location: shell\IShellImageData_GetRawDataFormat.htm
tech.root: shell
ms.assetid: c09c6833-501d-4f27-9d59-3ca9aed9d0d1
ms.date: 12/05/2018
ms.keywords: GetRawDataFormat, GetRawDataFormat method [Windows Shell], GetRawDataFormat method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],GetRawDataFormat method, IShellImageData.GetRawDataFormat, IShellImageData::GetRawDataFormat, _shell_IShellImageData_GetRawDataFormat, shell.IShellImageData_GetRawDataFormat, shimgdata/IShellImageData::GetRawDataFormat
req.header: shimgdata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shimgdata.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellImageData::GetRawDataFormat
 - shimgdata/IShellImageData::GetRawDataFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageData.GetRawDataFormat
---

# IShellImageData::GetRawDataFormat


## -description

Retrieves a GUID that identifies the format of the image.

## -parameters

### -param pDataFormat [out]

Type: <b>GUID*</b>

A pointer to a value indicating the format. This value is valid only when the method returns S_OK.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The image has not been decoded or the decoding process failed.

</td>
</tr>
</table>

## -remarks

GUIDs that identify various file formats are defined in Gdiplusimaging.h.

