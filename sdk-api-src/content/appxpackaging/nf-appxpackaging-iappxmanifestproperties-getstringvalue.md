---
UID: NF:appxpackaging.IAppxManifestProperties.GetStringValue
title: IAppxManifestProperties::GetStringValue (appxpackaging.h)
description: Gets the value of the specified string element in the properties section.
helpviewer_keywords: ["GetStringValue","GetStringValue method [App packaging and management]","GetStringValue method [App packaging and management]","IAppxManifestProperties interface","IAppxManifestProperties interface [App packaging and management]","GetStringValue method","IAppxManifestProperties.GetStringValue","IAppxManifestProperties::GetStringValue","appxpackaging/IAppxManifestProperties::GetStringValue","appxpkg.iappxmanifestproperties_getstringvalue"]
old-location: appxpkg\iappxmanifestproperties_getstringvalue.htm
tech.root: appxpkg
ms.assetid: 3EF2D8A2-37B2-4E57-9FD3-DA05FA90749C
ms.date: 12/05/2018
ms.keywords: GetStringValue, GetStringValue method [App packaging and management], GetStringValue method [App packaging and management],IAppxManifestProperties interface, IAppxManifestProperties interface [App packaging and management],GetStringValue method, IAppxManifestProperties.GetStringValue, IAppxManifestProperties::GetStringValue, appxpackaging/IAppxManifestProperties::GetStringValue, appxpkg.iappxmanifestproperties_getstringvalue
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
 - IAppxManifestProperties::GetStringValue
 - appxpackaging/IAppxManifestProperties::GetStringValue
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
 - IAppxManifestProperties.GetStringValue
---

# IAppxManifestProperties::GetStringValue


## -description

Gets the value of the specified string element in the properties section.

## -parameters

### -param name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The name of the string element. Valid values include:

<p class="indent">"Description"

<p class="indent">"DisplayName"

<p class="indent">"Logo"

<p class="indent">"PublisherDisplayName"

### -param value [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a>*</b>

The value of the specified element.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If a valid string property with this name is not defined in the manifest, this method  returns <b>E_INVALIDARG</b> and  <i>value</i> receives a null string.

The caller must free the memory allocated for <i>value</i> using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestproperties">IAppxManifestProperties</a>