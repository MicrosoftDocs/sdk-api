---
UID: NN:appxpackaging.IAppxPackageEditor
title: IAppxPackageEditor
author: windows-sdk-content
description: Provides functionality to edit app packages.
old-location: appxpkg\iappxpackageeditor.htm
old-project: appxpkg
ms.assetid: 37D9494A-A5C0-4ABA-99BC-7F9B10E8D06C
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: IAppxPackageEditor, IAppxPackageEditor interface [App packaging and management], IAppxPackageEditor interface [App packaging and management],described, appxpackaging/IAppxPackageEditor, appxpkg.iappxpackageeditor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: appxpackaging.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxPackageEditor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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

