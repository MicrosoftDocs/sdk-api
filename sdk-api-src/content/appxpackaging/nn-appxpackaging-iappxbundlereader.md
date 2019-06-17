---
UID: NN:appxpackaging.IAppxBundleReader
title: IAppxBundleReader (appxpackaging.h)
author: windows-sdk-content
description: Provides a read-only object model for bundle packages.
old-location: appxpkg\iappxbundlereader.htm
tech.root: appxpkg
ms.assetid: 3847AF32-D8E4-4BB2-9FBC-7CFAEF2CA664
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppxBundleReader, IAppxBundleReader interface [App packaging and management], IAppxBundleReader interface [App packaging and management],described, appxpackaging/IAppxBundleReader, appxpkg.iappxbundlereader
ms.topic: interface
f1_keywords: ["appxpackaging/IAppxBundleReader"]
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IAppxBundleReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBundleReader interface


## -description


Provides a read-only object model for bundle packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleReader</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBundleReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlereader-getblockmap">GetBlockMap</a>
</td>
<td align="left" width="63%">
Retrieves a read-only block map object from the bundle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlereader-getfootprintfile">GetFootprintFile</a>
</td>
<td align="left" width="63%">
Retrieves the specified type of footprint file from the bundle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlereader-getmanifest">GetManifest</a>
</td>
<td align="left" width="63%">
Retrieves a read-only manifest object from the bundle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlereader-getpayloadpackage">GetPayloadPackage</a>
</td>
<td align="left" width="63%">
Retrieves an appx file object for the payload package with the specified file name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlereader-getpayloadpackages">GetPayloadPackages</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator that iterates over the list of all payload packages in the bundle. 

</td>
</tr>
</table> 


## -remarks



You can use the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlefactory-createbundlereader">CreateBundleReader</a> method of the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlefactory">IAppxBundleFactory</a> interface to retrieve the <b>IAppxBundleReader</b> object. 

Through <b>IAppxBundleReader</b>, you can retrieve both footprint files, such as the bundle’s manifest, block map, and signature, and app packages that are contained in the bundle.



