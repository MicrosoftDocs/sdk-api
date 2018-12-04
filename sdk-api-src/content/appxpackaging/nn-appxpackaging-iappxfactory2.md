---
UID: NN:appxpackaging.IAppxFactory2
title: IAppxFactory2
author: windows-sdk-content
description: Creates objects for reading and writing app packages.
old-location: appxpkg\iappxfactory2.htm
tech.root: appxpkg
ms.assetid: 01B11591-F854-4A39-8EDD-A5140235CA0B
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IAppxFactory2, IAppxFactory2 interface [App packaging and management], IAppxFactory2 interface [App packaging and management],described, appxpackaging/IAppxFactory2, appxpkg.iappxfactory2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxFactory2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxFactory2 interface


## -description


Creates objects for reading and writing app packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxFactory2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxFactory2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxFactory2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42453BD7-AB65-49E0-86C0-4F96B4234397">CreateContentGroupMapReader</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/45C6F61E-8CF6-4188-9715-3954562F8AB0">IAppxContentGroupMapReader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4BFF656D-4B89-4D05-9A41-44400F75E8BC">CreateContentGroupMapWriter</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/A9B3992C-D3D1-4190-9314-A21E388E88BA">IAppxContentGroupMapWriter</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DB0FFB8D-A9DB-4B9C-B277-76623ECA3D6B">CreateSourceContentGroupMapReader</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/EA0DF7E6-C4EF-4A58-A13F-EB3789239084">IAppxSourceContentGroupMapReader</a>.

</td>
</tr>
</table> 

