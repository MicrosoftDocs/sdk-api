---
UID: NN:appxpackaging.IAppxBundleManifestReader2
title: IAppxBundleManifestReader2
author: windows-sdk-content
description: Provides a read-only object model for manifests of bundle packages.
old-location: appxpkg\iappxbundlemanifestreader2.htm
old-project: appxpkg
ms.assetid: 37236CED-F32F-4726-B945-F7359AEFF030
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IAppxBundleManifestReader2, IAppxBundleManifestReader2 interface [App packaging and management], IAppxBundleManifestReader2 interface [App packaging and management],described, appxpackaging/IAppxBundleManifestReader2, appxpkg.iappxbundlemanifestreader2
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxBundleManifestReader2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleManifestReader2 interface


## -description


Provides a read-only object model for manifests of bundle packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleManifestReader2</b> interface inherits from <a href="https://msdn.microsoft.com/2ABC7B5A-6489-4B52-B1C4-22D432EC9947">IAppxBundleManifestReader</a>. <b>IAppxBundleManifestReader2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleManifestReader2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26246BB1-7FE7-462F-9731-D8AD32373184">GetOptionalBundles</a>
</td>
<td align="left" width="63%">
Retrieves an object that represents the &lt;OptionalBundles&gt; element under the root &lt;Bundle&gt; element. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2ABC7B5A-6489-4B52-B1C4-22D432EC9947">IAppxBundleManifestReader</a>
 

 

