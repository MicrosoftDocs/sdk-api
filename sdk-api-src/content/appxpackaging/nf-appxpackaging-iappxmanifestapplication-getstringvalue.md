---
UID: NF:appxpackaging.IAppxManifestApplication.GetStringValue
title: IAppxManifestApplication::GetStringValue (appxpackaging.h)
description: Gets the value of a string element in the application metadata section of the manifest.
helpviewer_keywords: ["GetStringValue","GetStringValue method [App packaging and management]","GetStringValue method [App packaging and management]","IAppxManifestApplication interface","IAppxManifestApplication interface [App packaging and management]","GetStringValue method","IAppxManifestApplication.GetStringValue","IAppxManifestApplication::GetStringValue","appxpackaging/IAppxManifestApplication::GetStringValue","appxpkg.iappxmanifestapplication_getstringvalue"]
old-location: appxpkg\iappxmanifestapplication_getstringvalue.htm
tech.root: appxpkg
ms.assetid: 968EE95D-D1FC-42D7-B533-99062C26B4C3
ms.date: 12/05/2018
ms.keywords: GetStringValue, GetStringValue method [App packaging and management], GetStringValue method [App packaging and management],IAppxManifestApplication interface, IAppxManifestApplication interface [App packaging and management],GetStringValue method, IAppxManifestApplication.GetStringValue, IAppxManifestApplication::GetStringValue, appxpackaging/IAppxManifestApplication::GetStringValue, appxpkg.iappxmanifestapplication_getstringvalue
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
 - IAppxManifestApplication::GetStringValue
 - appxpackaging/IAppxManifestApplication::GetStringValue
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
 - IAppxManifestApplication.GetStringValue
---

# IAppxManifestApplication::GetStringValue


## -description

Gets the string value of an element or attribute in the application metadata section of the manifest.

## -parameters

### -param name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The name of the element or attribute value to get from the application metadata. Supported names include:

* AppListEntry
* BackgroundColor
* DefaultSize
* Description
* DisplayName
* EntryPoint
* Executable
* ForegroundText
* ID
* LockScreenLogo
* LockScreenNotification
* Logo
* MinWidth
* ShortName
* SmallLogo
* Square150x150Logo
* Square30x30Logo
* Square310x310Logo
* Square44x44Logo
* Square70x70Logo
* Square71x71Logo
* StartPage
* Tall150x310Logo
* VisualGroup
* WideLogo
* Wide310x150Logo

Refer to the [schema](/uwp/schemas/appxpackage/uapmanifestschema/schema-root) to determine where these values are being read from in the manifest.

### -param value [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a>*</b>

The value of the requested element or attribute.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

If the *name* parameter is not a supported name of an element or attribute in the manifest, this method returns **E_INVALIDARG**. If the *name* parameter is supported but the element or attribute is not found in the manifest, this method returns **S_OK** and the return value of the *value* parameter is **NULL**.

The caller must free the memory allocated for *value* using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestapplication">IAppxManifestApplication</a>