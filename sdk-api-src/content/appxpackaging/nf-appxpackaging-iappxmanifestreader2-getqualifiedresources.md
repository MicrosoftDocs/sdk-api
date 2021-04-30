---
UID: NF:appxpackaging.IAppxManifestReader2.GetQualifiedResources
title: IAppxManifestReader2::GetQualifiedResources (appxpackaging.h)
description: Gets an enumerator that iterates through the qualified resources that are defined in the manifest.
helpviewer_keywords: ["GetQualifiedResources","GetQualifiedResources method [App packaging and management]","GetQualifiedResources method [App packaging and management]","IAppxManifestReader2 interface","IAppxManifestReader2 interface [App packaging and management]","GetQualifiedResources method","IAppxManifestReader2.GetQualifiedResources","IAppxManifestReader2::GetQualifiedResources","appxpackaging/IAppxManifestReader2::GetQualifiedResources","appxpkg.iappxmanifestreader2_getqualifiedresources"]
old-location: appxpkg\iappxmanifestreader2_getqualifiedresources.htm
tech.root: appxpkg
ms.assetid: C712DA82-CA4F-4C5B-A391-3B40D5EE61C4
ms.date: 12/05/2018
ms.keywords: GetQualifiedResources, GetQualifiedResources method [App packaging and management], GetQualifiedResources method [App packaging and management],IAppxManifestReader2 interface, IAppxManifestReader2 interface [App packaging and management],GetQualifiedResources method, IAppxManifestReader2.GetQualifiedResources, IAppxManifestReader2::GetQualifiedResources, appxpackaging/IAppxManifestReader2::GetQualifiedResources, appxpkg.iappxmanifestreader2_getqualifiedresources
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
 - IAppxManifestReader2::GetQualifiedResources
 - appxpackaging/IAppxManifestReader2::GetQualifiedResources
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
 - IAppxManifestReader2.GetQualifiedResources
---

# IAppxManifestReader2::GetQualifiedResources


## -description

Gets an enumerator that iterates through the qualified resources that are defined in the manifest.

## -parameters

### -param resources [out, retval]

Type: <b><a href="/previous-versions/dn280306(v=vs.85)">IAppxManifestQualifiedResourcesEnumerator</a>**</b>

The enumerator that iterates through the qualified resources.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

Resources are specified using the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-resources">Resources</a> element in the manifest.

Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method when you have finished using the <i>resources</i> object.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader2">IAppxManifestReader2</a>