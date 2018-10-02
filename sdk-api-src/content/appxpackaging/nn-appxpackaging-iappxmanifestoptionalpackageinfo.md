---
UID: NN:appxpackaging.IAppxManifestOptionalPackageInfo
title: IAppxManifestOptionalPackageInfo
author: windows-sdk-content
description: Provides access to attribute values of the optional package information.
old-location: appxpkg\iappxmanifestoptionalpackageinfo.htm
tech.root: appxpkg
ms.assetid: 2B21676C-90AF-418D-8213-065EBB6C165C
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IAppxManifestOptionalPackageInfo, IAppxManifestOptionalPackageInfo interface [App packaging and management], IAppxManifestOptionalPackageInfo interface [App packaging and management],described, appxpackaging/IAppxManifestOptionalPackageInfo, appxpkg.iappxmanifestoptionalpackageinfo
ms.prod: windows
ms.technology: windows-sdk
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
 - IAppxManifestOptionalPackageInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxManifestOptionalPackageInfo interface


## -description


Provides access to attribute values of the optional package information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestOptionalPackageInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxManifestOptionalPackageInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestOptionalPackageInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E52E411C-0A3E-4DA3-B25D-14E761FEF676">GetIsOptionalPackage</a>
</td>
<td align="left" width="63%">
Determines whether the package is optional.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95CD6739-06B2-4862-8313-4133AFBFD583">GetMainPackageName</a>
</td>
<td align="left" width="63%">
Gets the main package name from the optional package.

</td>
</tr>
</table> 

