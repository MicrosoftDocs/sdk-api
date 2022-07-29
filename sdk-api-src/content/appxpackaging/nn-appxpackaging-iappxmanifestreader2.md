---
UID: NN:appxpackaging.IAppxManifestReader2
title: IAppxManifestReader2 (appxpackaging.h)
description: Represents an object model of the package manifest that provides methods to access manifest elements and attributes. (IAppxManifestReader2)
helpviewer_keywords: ["IAppxManifestReader2","IAppxManifestReader2 interface [App packaging and management]","IAppxManifestReader2 interface [App packaging and management]","described","appxpackaging/IAppxManifestReader2","appxpkg.iappxmanifestreader2"]
old-location: appxpkg\iappxmanifestreader2.htm
tech.root: appxpkg
ms.assetid: B10A1ACB-12F4-4338-A6D6-6D2B829F9D62
ms.date: 12/05/2018
ms.keywords: IAppxManifestReader2, IAppxManifestReader2 interface [App packaging and management], IAppxManifestReader2 interface [App packaging and management],described, appxpackaging/IAppxManifestReader2, appxpkg.iappxmanifestreader2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxManifestReader2
 - appxpackaging/IAppxManifestReader2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxManifestReader2
---

# IAppxManifestReader2 interface


## -description

Represents an object model of the package manifest that provides methods to access manifest elements and attributes.

## -inheritance

The <b>IAppxManifestReader2</b> interface inherits from <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>. <b>IAppxManifestReader2</b> also has these types of members:

## -remarks

<div class="alert"><b>Note</b>  Starting with Windows 8.1, we recommend not to use <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getresources">IAppxManifestReader::GetResources</a> anymore to only iterate over the <b>Language</b> values in the manifest. Instead, use <b>IAppxManifestReader2::GetResources</b> because it iterates over other resource qualifiers as well, such as, <b>Scale</b> and <b>DXFeatureLevel</b>. </div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>
