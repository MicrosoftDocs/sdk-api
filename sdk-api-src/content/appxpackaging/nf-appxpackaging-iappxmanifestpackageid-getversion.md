---
UID: NF:appxpackaging.IAppxManifestPackageId.GetVersion
title: IAppxManifestPackageId::GetVersion (appxpackaging.h)
description: Gets the version of the package as defined in the manifest.
helpviewer_keywords: ["GetVersion","GetVersion method [App packaging and management]","GetVersion method [App packaging and management]","IAppxManifestPackageId interface","IAppxManifestPackageId interface [App packaging and management]","GetVersion method","IAppxManifestPackageId.GetVersion","IAppxManifestPackageId::GetVersion","appxpackaging/IAppxManifestPackageId::GetVersion","appxpkg.iappxmanifestpackageid_getversion"]
old-location: appxpkg\iappxmanifestpackageid_getversion.htm
tech.root: appxpkg
ms.assetid: 85684359-9244-4130-BF0F-56DDB6427345
ms.date: 12/05/2018
ms.keywords: GetVersion, GetVersion method [App packaging and management], GetVersion method [App packaging and management],IAppxManifestPackageId interface, IAppxManifestPackageId interface [App packaging and management],GetVersion method, IAppxManifestPackageId.GetVersion, IAppxManifestPackageId::GetVersion, appxpackaging/IAppxManifestPackageId::GetVersion, appxpkg.iappxmanifestpackageid_getversion
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
 - IAppxManifestPackageId::GetVersion
 - appxpackaging/IAppxManifestPackageId::GetVersion
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
 - IAppxManifestPackageId.GetVersion
---

# IAppxManifestPackageId::GetVersion


## -description

Gets the version of the package as defined in the manifest.

## -parameters

### -param packageVersion [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a>*</b>

The version of the package.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

The version is specified using the <b>Version</b> attribute of the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity">Identity</a> element in the package manifest. The specification in the manifest is in quad notation:

<i>major</i>.<i>minor</i>.<i>build</i>.<i>revision</i>

This method converts this notation to a <b>UINT64</b> value as follows:

<ul>
<li>The high-order word contains the major version</li>
<li>The next word contains the minor version</li>
<li>The next word contains the build number</li>
<li>The low-order word contains the revision</li>
</ul>

#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackageid">IAppxManifestPackageId</a>