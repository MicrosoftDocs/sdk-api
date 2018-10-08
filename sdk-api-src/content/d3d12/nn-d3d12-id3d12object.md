---
UID: NN:d3d12.ID3D12Object
title: ID3D12Object
author: windows-sdk-content
description: An interface from which ID3D12Device and ID3D12DeviceChild inherit from. It provides methods to associate private data and annotate object names.
old-location: direct3d12\id3d12object.htm
tech.root: direct3d12
ms.assetid: D2B2BC74-E89D-4D3A-8808-6E4A94992769
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ID3D12Object, ID3D12Object interface, ID3D12Object interface,described, d3d12/ID3D12Object, direct3d12.id3d12object
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
 - ID3D12Object
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Object interface


## -description


An interface from which <a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a> and <a href="https://msdn.microsoft.com/AED60281-A6E4-4AAD-A106-6CA6E9BAEB9A">ID3D12DeviceChild</a> inherit from. It provides methods to associate private data and annotate object names.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Object</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12Object</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12Object</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B2F1FFBE-1680-40D7-8B99-07FCA3F3EA0B">GetPrivateData</a>
</td>
<td align="left" width="63%">
Gets application-defined data from a device object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A1DEEB16-BF75-4391-ADF0-AC22EECBC71A">SetName</a>
</td>
<td align="left" width="63%">
Associates a name with the device object.
          This name is for use in debug diagnostics and tools.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1B3E8202-7CB3-4D9F-A1AE-70E66652773C">SetPrivateData</a>
</td>
<td align="left" width="63%">
Sets application-defined data to a device object and associates that data with an application-defined <b>GUID</b>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B03B9420-7E85-4C1A-858C-37B20E4D9B52">SetPrivateDataInterface</a>
</td>
<td align="left" width="63%">
Associates an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>-derived interface with the device object and associates that interface with an application-defined <b>GUID</b>.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

