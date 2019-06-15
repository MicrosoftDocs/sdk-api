---
UID: NN:appxpackaging.IAppxPackageEditor
title: IAppxPackageEditor (appxpackaging.h)
author: windows-sdk-content
description: Provides functionality to edit app packages.
old-location: appxpkg\iappxpackageeditor.htm
tech.root: appxpkg
ms.assetid: 37D9494A-A5C0-4ABA-99BC-7F9B10E8D06C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppxPackageEditor, IAppxPackageEditor interface [App packaging and management], IAppxPackageEditor interface [App packaging and management],described, appxpackaging/IAppxPackageEditor, appxpkg.iappxpackageeditor
ms.topic: interface
f1_keywords: ["appxpackaging/IAppxPackageEditor"]
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
 - IAppxPackageEditor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxPackageEditor interface


## -description


Provides functionality to edit app packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxPackageEditor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxPackageEditor</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackageeditor-createdeltapackage">CreateDeltaPackage</a>
</td>
<td align="left" width="63%">
Creates a delta package from the differences in the updated package and the baseline package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackageeditor-createdeltapackageusingbaselineblockmap">CreateDeltaPackageUsingBaselineBlockMap</a>
</td>
<td align="left" width="63%">
Creates a delta package from the differences in the updated package and the baseline block map.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackageeditor-updateencryptedpackage">UpdateEncryptedPackage</a>
</td>
<td align="left" width="63%">
Updates an encrypted app package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackageeditor-updatepackage">UpdatePackage</a>
</td>
<td align="left" width="63%">
Updates an app package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackageeditor-updatepackagemanifest">UpdatePackageManifest</a>
</td>
<td align="left" width="63%">
Updates an app package manifest.

</td>
</tr>
</table> 

