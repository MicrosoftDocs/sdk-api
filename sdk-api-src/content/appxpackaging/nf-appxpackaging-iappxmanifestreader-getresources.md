---
UID: NF:appxpackaging.IAppxManifestReader.GetResources
title: IAppxManifestReader::GetResources (appxpackaging.h)
description: Gets an enumerator that iterates through the resources defined in the manifest.
helpviewer_keywords: ["GetResources","GetResources method [App packaging and management]","GetResources method [App packaging and management]","IAppxManifestReader interface","IAppxManifestReader interface [App packaging and management]","GetResources method","IAppxManifestReader.GetResources","IAppxManifestReader::GetResources","appxpackaging/IAppxManifestReader::GetResources","appxpkg.iappxmanifestreader_getresources"]
old-location: appxpkg\iappxmanifestreader_getresources.htm
tech.root: appxpkg
ms.assetid: 2F0109C2-99F5-4AEE-9596-153764FA8FA3
ms.date: 12/05/2018
ms.keywords: GetResources, GetResources method [App packaging and management], GetResources method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetResources method, IAppxManifestReader.GetResources, IAppxManifestReader::GetResources, appxpackaging/IAppxManifestReader::GetResources, appxpkg.iappxmanifestreader_getresources
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
 - IAppxManifestReader::GetResources
 - appxpackaging/IAppxManifestReader::GetResources
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
 - IAppxManifestReader.GetResources
---

# IAppxManifestReader::GetResources


## -description

Gets an enumerator that iterates through the resources defined in the manifest.

## -parameters

### -param resources [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestresourcesenumerator">IAppxManifestResourcesEnumerator</a>**</b>

The enumerator that iterates through the resources.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

Resources are specified using the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-resources">Resources</a> element in the manifest.

Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method when you have finished using the <i>resources</i> object.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>