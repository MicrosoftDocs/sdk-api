---
UID: NN:appxpackaging.IAppxBundleManifestOptionalBundleInfo
title: IAppxBundleManifestOptionalBundleInfo
author: windows-sdk-content
description: Provides a read-only object model for an &lt;OptionalBundle&gt; element in a bundle package manifest.
old-location: appxpkg\iappxbundlemanifestoptionalbundleinfo.htm
old-project: appxpkg
ms.assetid: C9DC823D-46D5-4459-A20A-0969D20C6E9E
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: IAppxBundleManifestOptionalBundleInfo, IAppxBundleManifestOptionalBundleInfo interface [App packaging and management], IAppxBundleManifestOptionalBundleInfo interface [App packaging and management],described, appxpackaging/IAppxBundleManifestOptionalBundleInfo, appxpkg.iappxbundlemanifestoptionalbundleinfo
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
tech.root: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxBundleManifestOptionalBundleInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleManifestOptionalBundleInfo interface


## -description


Provides a read-only object model for an &lt;OptionalBundle&gt; element in a bundle package manifest. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleManifestOptionalBundleInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxBundleManifestOptionalBundleInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleManifestOptionalBundleInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926842">GetFileName</a>
</td>
<td align="left" width="63%">
Retrieves the file-name attribute of the &lt;OptionalBundle&gt;.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57C8FB41-0218-4768-8E84-4ABF63EB94E8">GetPackageId</a>
</td>
<td align="left" width="63%">
Retrieves an object that represents the identity of the &lt;OptionalBundle&gt;.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6D5028BF-7C74-4F74-9600-0A423FDC6E85">GetPackageInfoItems</a>
</td>
<td align="left" width="63%">
Retrieves optional packages in the bundle.

</td>
</tr>
</table> 

