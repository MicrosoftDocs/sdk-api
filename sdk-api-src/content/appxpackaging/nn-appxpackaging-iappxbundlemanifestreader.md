---
UID: NN:appxpackaging.IAppxBundleManifestReader
title: IAppxBundleManifestReader
author: windows-sdk-content
description: Provides a read-only object model for manifests of bundle packages.
old-location: appxpkg\iappxbundlemanifestreader.htm
old-project: appxpkg
ms.assetid: 2ABC7B5A-6489-4B52-B1C4-22D432EC9947
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: IAppxBundleManifestReader, IAppxBundleManifestReader interface [App packaging and management], IAppxBundleManifestReader interface [App packaging and management],described, appxpackaging/IAppxBundleManifestReader, appxpkg.iappxbundlemanifestreader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxBundleManifestReader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleManifestReader interface


## -description


Provides a read-only object model for manifests of bundle packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleManifestReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxBundleManifestReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleManifestReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B1D8AF8D-A80B-4F28-A9AA-A798D309D6E0">GetPackageId</a>
</td>
<td align="left" width="63%">
Retrieves an object that represents the &lt;Identity&gt; element under the root &lt;Bundle&gt; element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D216C27E-5B73-49B5-90A8-11187C129264">GetPackageInfoItems</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator over all the &lt;Package&gt; elements under the &lt;Packages&gt; element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DC276734-3837-466E-ADBA-60B68356504E">GetStream</a>
</td>
<td align="left" width="63%">
Gets the raw XML document without any preprocessing.

</td>
</tr>
</table> 

