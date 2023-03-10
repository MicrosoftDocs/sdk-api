---
UID: NF:appxpackaging.IAppxManifestReader.GetApplications
title: IAppxManifestReader::GetApplications (appxpackaging.h)
description: Gets an enumerator that iterates through the applications defined in the manifest.
helpviewer_keywords: ["GetApplications","GetApplications method [App packaging and management]","GetApplications method [App packaging and management]","IAppxManifestReader interface","IAppxManifestReader interface [App packaging and management]","GetApplications method","IAppxManifestReader.GetApplications","IAppxManifestReader::GetApplications","appxpackaging/IAppxManifestReader::GetApplications","appxpkg.iappxmanifestreader_getapplications"]
old-location: appxpkg\iappxmanifestreader_getapplications.htm
tech.root: appxpkg
ms.assetid: EC575692-93D6-43F1-857B-9A27DD50B8FC
ms.date: 12/05/2018
ms.keywords: GetApplications, GetApplications method [App packaging and management], GetApplications method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetApplications method, IAppxManifestReader.GetApplications, IAppxManifestReader::GetApplications, appxpackaging/IAppxManifestReader::GetApplications, appxpkg.iappxmanifestreader_getapplications
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
 - IAppxManifestReader::GetApplications
 - appxpackaging/IAppxManifestReader::GetApplications
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
 - IAppxManifestReader.GetApplications
---

# IAppxManifestReader::GetApplications


## -description

Gets an enumerator that iterates through the applications defined in the manifest.

## -parameters

### -param applications [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestapplicationsenumerator">IAppxManifestApplicationsEnumerator</a>**</b>

The enumerator that iterates through the applications.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If no applications are defined in the manifest, this method returns <b>S_OK</b> with an empty <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestapplicationsenumerator">IAppxManifestApplicationsEnumerator</a> object.

Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method when you have finished using the <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a> object.


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>