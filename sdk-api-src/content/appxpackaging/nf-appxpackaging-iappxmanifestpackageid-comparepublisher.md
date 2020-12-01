---
UID: NF:appxpackaging.IAppxManifestPackageId.ComparePublisher
title: IAppxManifestPackageId::ComparePublisher (appxpackaging.h)
description: Compares the specified publisher with the publisher defined in the manifest.
helpviewer_keywords: ["ComparePublisher","ComparePublisher method [App packaging and management]","ComparePublisher method [App packaging and management]","IAppxManifestPackageId interface","IAppxManifestPackageId interface [App packaging and management]","ComparePublisher method","IAppxManifestPackageId.ComparePublisher","IAppxManifestPackageId::ComparePublisher","appxpackaging/IAppxManifestPackageId::ComparePublisher","appxpkg.iappxmanifestpackageid_comparepublisher"]
old-location: appxpkg\iappxmanifestpackageid_comparepublisher.htm
tech.root: appxpkg
ms.assetid: 8AC811D0-D5C5-47DF-92FD-C66BC018B668
ms.date: 12/05/2018
ms.keywords: ComparePublisher, ComparePublisher method [App packaging and management], ComparePublisher method [App packaging and management],IAppxManifestPackageId interface, IAppxManifestPackageId interface [App packaging and management],ComparePublisher method, IAppxManifestPackageId.ComparePublisher, IAppxManifestPackageId::ComparePublisher, appxpackaging/IAppxManifestPackageId::ComparePublisher, appxpkg.iappxmanifestpackageid_comparepublisher
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
 - IAppxManifestPackageId::ComparePublisher
 - appxpackaging/IAppxManifestPackageId::ComparePublisher
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
 - IAppxManifestPackageId.ComparePublisher
---

# IAppxManifestPackageId::ComparePublisher


## -description

Compares the specified publisher with the publisher defined in the manifest.

## -parameters

### -param other [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The publisher name to be compared.

### -param isSame [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

<b>TRUE</b> if the specified publisher matches the package publisher; <b>FALSE</b> otherwise.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

Publisher information is specified using the <b>Publisher</b> attribute of the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity">Identity</a> element in the package manifest.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackageid">IAppxManifestPackageId</a>