---
UID: NN:appxpackaging.IAppxManifestPackageId2
title: IAppxManifestPackageId2 (appxpackaging.h)
description: Provides access to the app package identity.
helpviewer_keywords: ["IAppxManifestPackageId2","IAppxManifestPackageId2 interface [App packaging and management]","IAppxManifestPackageId2 interface [App packaging and management]","described","appxpackaging/IAppxManifestPackageId2","appxpkg.iappxmanifestpackageid2"]
old-location: appxpkg\iappxmanifestpackageid2.htm
tech.root: appxpkg
ms.assetid: 27344514-B9B9-46EC-9A44-577C0C9361C8
ms.date: 12/05/2018
ms.keywords: IAppxManifestPackageId2, IAppxManifestPackageId2 interface [App packaging and management], IAppxManifestPackageId2 interface [App packaging and management],described, appxpackaging/IAppxManifestPackageId2, appxpkg.iappxmanifestpackageid2
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxManifestPackageId2
 - appxpackaging/IAppxManifestPackageId2
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
 - IAppxManifestPackageId2
---

# IAppxManifestPackageId2 interface


## -description

Provides access to the app package identity.

## -inheritance

The <b>IAppxManifestPackageId2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxManifestPackageId2</b> also has these types of members:

## -remarks

Package identity information is specified using the <b>Identity</b> element in the package manifest.

This object can be retrieved using the <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getpackageid">IAppxManifestReader::GetPackageId</a> method.
