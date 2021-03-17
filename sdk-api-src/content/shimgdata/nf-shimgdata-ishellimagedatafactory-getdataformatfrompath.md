---
UID: NF:shimgdata.IShellImageDataFactory.GetDataFormatFromPath
title: IShellImageDataFactory::GetDataFormatFromPath (shimgdata.h)
description: Determines a file's format based on its extension.
helpviewer_keywords: ["GetDataFormatFromPath","GetDataFormatFromPath method [Windows Shell]","GetDataFormatFromPath method [Windows Shell]","IShellImageDataFactory interface","IShellImageDataFactory interface [Windows Shell]","GetDataFormatFromPath method","IShellImageDataFactory.GetDataFormatFromPath","IShellImageDataFactory::GetDataFormatFromPath","_shell_IShellImageDataFactory_GetDataFormatFromPath","shell.IShellImageDataFactory_GetDataFormatFromPath","shimgdata/IShellImageDataFactory::GetDataFormatFromPath"]
old-location: shell\IShellImageDataFactory_GetDataFormatFromPath.htm
tech.root: shell
ms.assetid: ca6aa555-5997-43c6-84d1-35a24301d0a2
ms.date: 12/05/2018
ms.keywords: GetDataFormatFromPath, GetDataFormatFromPath method [Windows Shell], GetDataFormatFromPath method [Windows Shell],IShellImageDataFactory interface, IShellImageDataFactory interface [Windows Shell],GetDataFormatFromPath method, IShellImageDataFactory.GetDataFormatFromPath, IShellImageDataFactory::GetDataFormatFromPath, _shell_IShellImageDataFactory_GetDataFormatFromPath, shell.IShellImageDataFactory_GetDataFormatFromPath, shimgdata/IShellImageDataFactory::GetDataFormatFromPath
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
 - IShellImageDataFactory::GetDataFormatFromPath
 - shimgdata/IShellImageDataFactory::GetDataFormatFromPath
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
 - IShellImageDataFactory.GetDataFormatFromPath
---

# IShellImageDataFactory::GetDataFormatFromPath


## -description

Determines a file's format based on its extension.

## -parameters

### -param pszPath [in]

Type: <b>LPCWSTR</b>

A path to the file.

### -param pDataFormat [out]

Type: <b>GUID*</b>

A pointer to a GUID identifying the image format of the file.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise, including the following:

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
The <i>pszPath</i> parameter is <b>NULL</b>, the file name extension does not correspond to any defined GDI+ decoder, or an internal error has occurred. In any of these cases, <i>pDataFormat</i> is set to GUID_NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The internal object cannot be instantiated.

</td>
</tr>
</table>

## -remarks

<b>IShellImageDataFactory::GetDataFormatFromPath</b> should only be used to determine whether data can be saved to a particular format on the current system.

