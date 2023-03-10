---
UID: NF:shimgdata.IShellImageDataFactory.CreateImageFromStream
title: IShellImageDataFactory::CreateImageFromStream (shimgdata.h)
description: Creates an instance of the IShellImageData interface based on a given file stream.
helpviewer_keywords: ["CreateImageFromStream","CreateImageFromStream method [Windows Shell]","CreateImageFromStream method [Windows Shell]","IShellImageDataFactory interface","IShellImageDataFactory interface [Windows Shell]","CreateImageFromStream method","IShellImageDataFactory.CreateImageFromStream","IShellImageDataFactory::CreateImageFromStream","_shell_IShellImageDataFactory_CreateImageFromStream","shell.IShellImageDataFactory_CreateImageFromStream","shimgdata/IShellImageDataFactory::CreateImageFromStream"]
old-location: shell\IShellImageDataFactory_CreateImageFromStream.htm
tech.root: shell
ms.assetid: 009c4b46-0f2c-43ee-84be-017bf12b28e5
ms.date: 12/05/2018
ms.keywords: CreateImageFromStream, CreateImageFromStream method [Windows Shell], CreateImageFromStream method [Windows Shell],IShellImageDataFactory interface, IShellImageDataFactory interface [Windows Shell],CreateImageFromStream method, IShellImageDataFactory.CreateImageFromStream, IShellImageDataFactory::CreateImageFromStream, _shell_IShellImageDataFactory_CreateImageFromStream, shell.IShellImageDataFactory_CreateImageFromStream, shimgdata/IShellImageDataFactory::CreateImageFromStream
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
 - IShellImageDataFactory::CreateImageFromStream
 - shimgdata/IShellImageDataFactory::CreateImageFromStream
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
 - IShellImageDataFactory.CreateImageFromStream
---

# IShellImageDataFactory::CreateImageFromStream


## -description

Creates an instance of the <a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> interface based on a given file stream.

## -parameters

### -param pStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A pointer to the image stream.

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

If <i>pStream</i> is <b>NULL</b> or an invalid pointer, later calls to <a href="/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-decode">Decode</a> will cause an access violation.