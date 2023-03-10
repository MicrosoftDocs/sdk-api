---
UID: NN:appxpackaging.IAppxFactory
title: IAppxFactory (appxpackaging.h)
description: Creates objects for reading and writing app packages. (IAppxFactory)
helpviewer_keywords: ["IAppxFactory","IAppxFactory interface [App packaging and management]","IAppxFactory interface [App packaging and management]","described","appxpackaging/IAppxFactory","appxpkg.iappxfactory"]
old-location: appxpkg\iappxfactory.htm
tech.root: appxpkg
ms.assetid: 4EA79D44-7C26-4B65-81A1-394E1E540F34
ms.date: 12/05/2018
ms.keywords: IAppxFactory, IAppxFactory interface [App packaging and management], IAppxFactory interface [App packaging and management],described, appxpackaging/IAppxFactory, appxpkg.iappxfactory
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxFactory
 - appxpackaging/IAppxFactory
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
 - IAppxFactory
---

# IAppxFactory interface


## -description

Creates objects for reading and writing app packages.

## -inheritance

The <b>IAppxFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxFactory</b> also has these types of members:

## -remarks

The <b>IAppxFactory</b> interface provides factory methods to create readers and writers of app packages as well as methods to create readers for block maps and manifests outside of a package.


#### Examples

For examples, see:

<ul>
<li>
<a href="/windows/desktop/appxpkg/how-to-create-a-package">How to create an app  package</a>
</li>
<li>
<a href="/windows/desktop/appxpkg/how-to-extract-content-from-a-package">Quickstart: Extract app package contents</a>
</li>
<li>
<a href="/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>
</li>
</ul>
<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapreader">IAppxBlockMapReader</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagereader">IAppxPackageReader</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagewriter">IAppxPackageWriter</a>
