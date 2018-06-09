---
UID: NF:shimgdata.IShellImageDataFactory.CreateImageFromStream
title: IShellImageDataFactory::CreateImageFromStream
author: windows-sdk-content
description: Creates an instance of the IShellImageData interface based on a given file stream.
old-location: shell\IShellImageDataFactory_CreateImageFromStream.htm
old-project: shell
ms.assetid: 009c4b46-0f2c-43ee-84be-017bf12b28e5
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CreateImageFromStream, CreateImageFromStream method [Windows Shell], CreateImageFromStream method [Windows Shell],IShellImageDataFactory interface, IShellImageDataFactory interface [Windows Shell],CreateImageFromStream method, IShellImageDataFactory.CreateImageFromStream, IShellImageDataFactory::CreateImageFromStream, _shell_IShellImageDataFactory_CreateImageFromStream, shell.IShellImageDataFactory_CreateImageFromStream, shimgdata/IShellImageDataFactory::CreateImageFromStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: SHELL_UI_COMPONENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageDataFactory.CreateImageFromStream
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellImageDataFactory::CreateImageFromStream


## -description


Creates an instance of the <a href="https://msdn.microsoft.com/935e651c-4dcd-4317-847e-34adf656035c">IShellImageData</a> interface based on a given file stream.


## -parameters




### -param pStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

A pointer to the image stream.


### -param ppshimg [out]

Type: <b><a href="https://msdn.microsoft.com/935e651c-4dcd-4317-847e-34adf656035c">IShellImageData</a>**</b>

The address of a pointer to an instance of <a href="https://msdn.microsoft.com/935e651c-4dcd-4317-847e-34adf656035c">IShellImageData</a>.


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
The internal object does not support the <a href="https://msdn.microsoft.com/935e651c-4dcd-4317-847e-34adf656035c">IShellImageData</a> or <a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a> interfaces.

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



If <i>pStream</i> is <b>NULL</b> or an invalid pointer, later calls to <a href="https://msdn.microsoft.com/954424d6-cb90-46c1-a850-4e1113dfe2e4">Decode</a> will cause an access violation.



