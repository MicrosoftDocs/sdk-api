---
UID: NF:shimgdata.IShellImageDataFactory.CreateImageFromFile
title: IShellImageDataFactory::CreateImageFromFile (shimgdata.h)
description: Creates an instance of the IShellImageData interface based on a given file.
helpviewer_keywords: ["CreateImageFromFile","CreateImageFromFile method [Windows Shell]","CreateImageFromFile method [Windows Shell]","IShellImageDataFactory interface","IShellImageDataFactory interface [Windows Shell]","CreateImageFromFile method","IShellImageDataFactory.CreateImageFromFile","IShellImageDataFactory::CreateImageFromFile","_shell_IShellImageDataFactory_CreateImageFromFile","shell.IShellImageDataFactory_CreateImageFromFile","shimgdata/IShellImageDataFactory::CreateImageFromFile"]
old-location: shell\IShellImageDataFactory_CreateImageFromFile.htm
tech.root: shell
ms.assetid: 9d33f9ad-30ce-431c-aec3-c27a33cec008
ms.date: 12/05/2018
ms.keywords: CreateImageFromFile, CreateImageFromFile method [Windows Shell], CreateImageFromFile method [Windows Shell],IShellImageDataFactory interface, IShellImageDataFactory interface [Windows Shell],CreateImageFromFile method, IShellImageDataFactory.CreateImageFromFile, IShellImageDataFactory::CreateImageFromFile, _shell_IShellImageDataFactory_CreateImageFromFile, shell.IShellImageDataFactory_CreateImageFromFile, shimgdata/IShellImageDataFactory::CreateImageFromFile
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
 - IShellImageDataFactory::CreateImageFromFile
 - shimgdata/IShellImageDataFactory::CreateImageFromFile
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
 - IShellImageDataFactory.CreateImageFromFile
---

# IShellImageDataFactory::CreateImageFromFile


## -description

Creates an instance of the <a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> interface based on a given file.

## -parameters

### -param pszPath [in]

Type: <b>LPCWSTR</b>

The path of the file containing the image. If this parameter is <b>NULL</b>, an unhandled exception results.

### -param ppshimg [out]

Type: <b><a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a>**</b>

The address of a pointer to an instance of <a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a>.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The internal object cannot be instantiated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The internal object does not support the <a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> or <a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a> interfaces.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppshimg</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

An access violation occurs if <i>pszPath</i> is <b>NULL</b>.