---
UID: NN:appxpackaging.IAppxPackageReader
title: IAppxPackageReader (appxpackaging.h)
description: Provides a read-only object model for app packages.
old-location: appxpkg\iappxpackagereader.htm
tech.root: appxpkg
ms.assetid: D34D0909-BE2B-4182-8C3D-36A4E8DDC820
ms.date: 12/05/2018
ms.keywords: IAppxPackageReader, IAppxPackageReader interface [App packaging and management], IAppxPackageReader interface [App packaging and management],described, appxpackaging/IAppxPackageReader, appxpkg.iappxpackagereader
f1_keywords:
- appxpackaging/IAppxPackageReader
dev_langs:
- c++
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
- IAppxPackageReader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxPackageReader interface


## -description


Provides a read-only object model for app packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxPackageReader</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxPackageReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxPackageReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getblockmap">GetBlockMap</a>
</td>
<td align="left" width="63%">
Retrieves the block map object model of the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getfootprintfile">GetFootprintFile</a>
</td>
<td align="left" width="63%">
Retrieves a footprint file from the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getmanifest">GetManifest</a>
</td>
<td align="left" width="63%">
Retrieves the object model of the app manifest of the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getpayloadfile">GetPayloadFile</a>
</td>
<td align="left" width="63%">
Retrieves a payload file from the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getpayloadfiles">GetPayloadFiles</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator that iterates through the payload files in the package.

</td>
</tr>
</table> 


## -remarks



The <b>IAppxPackageReader</b> interface provides the ability to access payload files from a package and to query metadata from footprint files. 

This object can be retrieved using the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfactory-createpackagereader">CreatePackageReader</a> method of the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfactory">IAppxFactory</a> interface.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/appxpkg/how-to-extract-content-from-a-package">Quickstart: Extract app package contents</a> and <a href="https://docs.microsoft.com/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagewriter">IAppxPackageWriter</a>
 

 

