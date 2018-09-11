---
UID: NF:shimgdata.IShellImageDataFactory.CreateIShellImageData
title: IShellImageDataFactory::CreateIShellImageData
author: windows-sdk-content
description: Creates an instance of the IShellImageData interface.
old-location: shell\IShellImageDataFactory_CreateIShellImageData.htm
tech.root: shell
ms.assetid: fdba8376-c878-4fc8-bedc-e73cfeef8b9b
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CreateIShellImageData, CreateIShellImageData method [Windows Shell], CreateIShellImageData method [Windows Shell],IShellImageDataFactory interface, IShellImageDataFactory interface [Windows Shell],CreateIShellImageData method, IShellImageDataFactory.CreateIShellImageData, IShellImageDataFactory::CreateIShellImageData, _shell_IShellImageDataFactory_CreateIShellImageData, shell.IShellImageDataFactory_CreateIShellImageData, shimgdata/IShellImageDataFactory::CreateIShellImageData
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageDataFactory.CreateIShellImageData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellImageDataFactory::CreateIShellImageData


## -description


Creates an instance of the <a href="https://msdn.microsoft.com/935e651c-4dcd-4317-847e-34adf656035c">IShellImageData</a> interface.


## -parameters




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
The internal object does not support <a href="https://msdn.microsoft.com/935e651c-4dcd-4317-847e-34adf656035c">IShellImageData</a>.

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
 



