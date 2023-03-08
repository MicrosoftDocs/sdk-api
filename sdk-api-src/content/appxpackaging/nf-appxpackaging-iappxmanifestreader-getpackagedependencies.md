---
UID: NF:appxpackaging.IAppxManifestReader.GetPackageDependencies
title: IAppxManifestReader::GetPackageDependencies (appxpackaging.h)
description: Gets an enumerator that iterates through dependencies defined in the manifest.
helpviewer_keywords: ["GetPackageDependencies","GetPackageDependencies method [App packaging and management]","GetPackageDependencies method [App packaging and management]","IAppxManifestReader interface","IAppxManifestReader interface [App packaging and management]","GetPackageDependencies method","IAppxManifestReader.GetPackageDependencies","IAppxManifestReader::GetPackageDependencies","appxpackaging/IAppxManifestReader::GetPackageDependencies","appxpkg.iappxmanifestreader_getpackagedependencies"]
old-location: appxpkg\iappxmanifestreader_getpackagedependencies.htm
tech.root: appxpkg
ms.assetid: C40276CC-8F97-4DCF-A5C4-193453B8FA02
ms.date: 12/05/2018
ms.keywords: GetPackageDependencies, GetPackageDependencies method [App packaging and management], GetPackageDependencies method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetPackageDependencies method, IAppxManifestReader.GetPackageDependencies, IAppxManifestReader::GetPackageDependencies, appxpackaging/IAppxManifestReader::GetPackageDependencies, appxpkg.iappxmanifestreader_getpackagedependencies
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
 - IAppxManifestReader::GetPackageDependencies
 - appxpackaging/IAppxManifestReader::GetPackageDependencies
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
 - IAppxManifestReader.GetPackageDependencies
---

# IAppxManifestReader::GetPackageDependencies


## -description

Gets an enumerator that iterates through dependencies defined in the manifest.

## -parameters

### -param dependencies [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackagedependenciesenumerator">IAppxManifestPackageDependenciesEnumerator</a>**</b>

The enumerator that iterates through the dependencies.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If no package dependencies are found in the manifest, this method returns <b>S_OK</b> with an empty enumerator.

Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method when you have finished using the <i>dependencies</i> object.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>