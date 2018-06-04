---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IAppxPackageEditor interface


## -description


Provides functionality to edit app packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxPackageEditor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxPackageEditor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxPackageEditor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40B41D47-674A-4842-8C6D-FBB661D12589">CreateDeltaPackage</a>
</td>
<td align="left" width="63%">
Creates a delta package from the differences in the updated package and the baseline package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33D1CEBA-A7F4-4506-B467-3610A3737B87">CreateDeltaPackageUsingBaselineBlockMap</a>
</td>
<td align="left" width="63%">
Creates a delta package from the differences in the updated package and the baseline block map.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4D5E2F4B-00CE-4A0A-A514-3B66EC3065ED">UpdateEncryptedPackage</a>
</td>
<td align="left" width="63%">
Updates an encrypted app package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/768D2997-A374-46FF-BA0D-14B266D3C83D">UpdatePackage</a>
</td>
<td align="left" width="63%">
Updates an app package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A30B3A7E-28FA-4780-9ED3-4F19887189E8">UpdatePackageManifest</a>
</td>
<td align="left" width="63%">
Updates an app package manifest.

</td>
</tr>
</table> 

