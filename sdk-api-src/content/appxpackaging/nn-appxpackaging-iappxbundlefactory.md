---
UID: NN:appxpackaging.IAppxBundleFactory
title: IAppxBundleFactory (appxpackaging.h)
author: windows-sdk-content
description: Creates objects for reading and writing bundle packages.
old-location: appxpkg\iappxbundlefactory.htm
tech.root: appxpkg
ms.assetid: 33A320BD-7B68-4C42-A776-25CC744C6652
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppxBundleFactory, IAppxBundleFactory interface [App packaging and management], IAppxBundleFactory interface [App packaging and management],described, appxpackaging/IAppxBundleFactory, appxpkg.iappxbundlefactory
ms.topic: interface
f1_keywords: ["appxpackaging/IAppxBundleFactory"]
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
 - IAppxBundleFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBundleFactory interface


## -description


Creates objects for reading and writing bundle packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBundleFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlefactory-createbundlemanifestreader">CreateBundleManifestReader</a>
</td>
<td align="left" width="63%">
Creates a read-only bundle manifest object from a standalone stream to AppxBundleManifest.xml.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlefactory-createbundlereader">CreateBundleReader</a>
</td>
<td align="left" width="63%">
Creates a read-only bundle object that reads its contents from an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlefactory-createbundlewriter">CreateBundleWriter</a>
</td>
<td align="left" width="63%">
Creates a write-only bundle object to which app packages can be added.  

</td>
</tr>
</table> 


## -remarks



The <b>IAppxBundleFactory</b> interface provides factory methods to create readers and writers of bundle packages as well as methods to create readers for manifests outside of a bundle. 

The <b>IAppxBundleFactory</b> interface is the main entry point to the Appx Bundle APIs.  



