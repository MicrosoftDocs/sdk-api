---
UID: NN:appxpackaging.IAppxBundleFactory
title: IAppxBundleFactory (appxpackaging.h)
description: Creates objects for reading and writing bundle packages.
helpviewer_keywords: ["IAppxBundleFactory","IAppxBundleFactory interface [App packaging and management]","IAppxBundleFactory interface [App packaging and management]","described","appxpackaging/IAppxBundleFactory","appxpkg.iappxbundlefactory"]
old-location: appxpkg\iappxbundlefactory.htm
tech.root: appxpkg
ms.assetid: 33A320BD-7B68-4C42-A776-25CC744C6652
ms.date: 12/05/2018
ms.keywords: IAppxBundleFactory, IAppxBundleFactory interface [App packaging and management], IAppxBundleFactory interface [App packaging and management],described, appxpackaging/IAppxBundleFactory, appxpkg.iappxbundlefactory
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
 - IAppxBundleFactory
 - appxpackaging/IAppxBundleFactory
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
 - IAppxBundleFactory
---

# IAppxBundleFactory interface


## -description

Creates objects for reading and writing bundle packages.

## -inheritance

The <b>IAppxBundleFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBundleFactory</b> also has these types of members:

## -remarks

The <b>IAppxBundleFactory</b> interface provides factory methods to create readers and writers of bundle packages as well as methods to create readers for manifests outside of a bundle. 

The <b>IAppxBundleFactory</b> interface is the main entry point to the Appx Bundle APIs.
