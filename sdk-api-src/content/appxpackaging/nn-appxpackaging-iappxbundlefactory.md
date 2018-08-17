---
UID: NN:appxpackaging.IAppxBundleFactory
title: IAppxBundleFactory
author: windows-sdk-content
description: Creates objects for reading and writing bundle packages.
old-location: appxpkg\iappxbundlefactory.htm
old-project: appxpkg
ms.assetid: 33A320BD-7B68-4C42-A776-25CC744C6652
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: IAppxBundleFactory, IAppxBundleFactory interface [App packaging and management], IAppxBundleFactory interface [App packaging and management],described, appxpackaging/IAppxBundleFactory, appxpkg.iappxbundlefactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: appxpackaging.h
req.include-header: 
req.redist: 
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
 - IAppxBundleFactory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleFactory interface


## -description


Creates objects for reading and writing bundle packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxBundleFactory</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8D537830-A8AA-4652-B6F2-F7A545B8877E">CreateBundleManifestReader</a>
</td>
<td align="left" width="63%">
Creates a read-only bundle manifest object from a standalone stream to AppxBundleManifest.xml.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3D9F7A0A-EF6A-4C99-B9A0-C618138DB5ED">CreateBundleReader</a>
</td>
<td align="left" width="63%">
Creates a read-only bundle object that reads its contents from an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E77392FB-69A1-41B0-8B44-F05F126214E0">CreateBundleWriter</a>
</td>
<td align="left" width="63%">
Creates a write-only bundle object to which app packages can be added.  

</td>
</tr>
</table> 


## -remarks



The <b>IAppxBundleFactory</b> interface provides factory methods to create readers and writers of bundle packages as well as methods to create readers for manifests outside of a bundle. 

The <b>IAppxBundleFactory</b> interface is the main entry point to the Appx Bundle APIs.  



