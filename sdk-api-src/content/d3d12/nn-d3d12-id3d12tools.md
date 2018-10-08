---
UID: NN:d3d12.ID3D12Tools
title: ID3D12Tools
author: windows-sdk-content
description: This interface is used to configure the runtime for tools such as PIX. Its not intended or supported for any other scenario.
old-location: direct3d12\id3d12tools.htm
tech.root: direct3d12
ms.assetid: F192AC22-1FD9-496D-9943-99FB424DD214
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ID3D12Tools, ID3D12Tools interface, ID3D12Tools interface,described, d3d12/ID3D12Tools, direct3d12.id3d12tools
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Tools
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Tools interface


## -description


This interface is used to configure the runtime for tools such as PIX. Its not intended or supported for any other scenario.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Tools</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12Tools</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12Tools</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35920253-1153-42AD-AEAC-2C646FF15879">EnableShaderInstrumentation</a>
</td>
<td align="left" width="63%">
This method enables tools such as PIX to instrument shaders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02A36358-5015-4CA1-B329-CCF074CF8F40">ShaderInstrumentationEnabled</a>
</td>
<td align="left" width="63%">
Determines whether shader instrumentation is enabled.

</td>
</tr>
</table> 


## -remarks



Do not use this interface in your application, its not intended or supported for any scenario other than to enable tooling such as PIX.

Developer Mode must be enabled for this interface to respond.




## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

