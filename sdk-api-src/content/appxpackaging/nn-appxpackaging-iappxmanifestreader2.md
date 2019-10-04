---
UID: NN:appxpackaging.IAppxManifestReader2
title: IAppxManifestReader2 (appxpackaging.h)
author: windows-sdk-content
description: Represents an object model of the package manifest that provides methods to access manifest elements and attributes.
old-location: appxpkg\iappxmanifestreader2.htm
tech.root: appxpkg
ms.assetid: B10A1ACB-12F4-4338-A6D6-6D2B829F9D62
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppxManifestReader2, IAppxManifestReader2 interface [App packaging and management], IAppxManifestReader2 interface [App packaging and management],described, appxpackaging/IAppxManifestReader2, appxpkg.iappxmanifestreader2
ms.topic: interface
f1_keywords: 
 - "appxpackaging/IAppxManifestReader2"
dev_langs:
 - c++
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
 - IAppxManifestReader2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxManifestReader2 interface


## -description


Represents an object model of the package manifest that provides methods to access manifest elements and attributes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestReader2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>. <b>IAppxManifestReader2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestReader2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader2-getqualifiedresources">GetQualifiedResources</a>
</td>
<td align="left" width="63%">
Gets an enumerator that iterates through the qualified resources that are defined in the manifest.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  Starting with Windows 8.1, we recommend not to use <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getresources">IAppxManifestReader::GetResources</a> anymore to only iterate over the <b>Language</b> values in the manifest. Instead, use <b>IAppxManifestReader2::GetResources</b> because it iterates over other resource qualifiers as well, such as, <b>Scale</b> and <b>DXFeatureLevel</b>. </div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>
 

 

