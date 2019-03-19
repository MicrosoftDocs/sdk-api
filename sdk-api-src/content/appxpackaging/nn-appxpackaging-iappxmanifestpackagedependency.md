---
UID: NN:appxpackaging.IAppxManifestPackageDependency
title: IAppxManifestPackageDependency (appxpackaging.h)
author: windows-sdk-content
description: Describes the dependency of one package on another package.
old-location: appxpkg\iappxmanifestpackagedependency.htm
tech.root: appxpkg
ms.assetid: 1A5515DA-4A9E-40EE-9AAC-F267DAE9DDBA
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAppxManifestPackageDependency, IAppxManifestPackageDependency interface [App packaging and management], IAppxManifestPackageDependency interface [App packaging and management],described, appxpackaging/IAppxManifestPackageDependency, appxpkg.iappxmanifestpackagedependency
ms.topic: interface
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IAppxManifestPackageDependency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxManifestPackageDependency interface


## -description


Describes the dependency of one package on another package.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestPackageDependency</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxManifestPackageDependency</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestPackageDependency</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/301053BA-A2DB-405C-9E2E-3817B2B5D7FD">GetMinVersion</a>
</td>
<td align="left" width="63%">
Gets the minimum version of the package on which the current package has a dependency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0B1888D7-04E6-4684-8131-8295EF2C598B">GetName</a>
</td>
<td align="left" width="63%">
Gets the name of the package on which the current package has a dependency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0E307900-EA2F-44A4-A379-3192A234E399">GetPublisher</a>
</td>
<td align="left" width="63%">
Gets the name of the publisher that produced the package on which the current package depends.

</td>
</tr>
</table> 


## -remarks



A dependency package is a package that the current package depends on, as specified in the package manifest using the <a href="https://msdn.microsoft.com/7f0800a1-f1dd-48c2-aba0-3701dd27d383">PackageDependency</a> element.




## -see-also




<a href="https://msdn.microsoft.com/A09709AE-301F-4457-8E02-1A88FB283A43">IAppxManifestPackageDependenciesEnumerator</a>
 

 

