---
UID: NF:appxpackaging.IAppxManifestProperties.GetBoolValue
title: IAppxManifestProperties::GetBoolValue (appxpackaging.h)
description: Gets the value of the specified Boolean element in the properties section.
helpviewer_keywords: ["GetBoolValue","GetBoolValue method [App packaging and management]","GetBoolValue method [App packaging and management]","IAppxManifestProperties interface","IAppxManifestProperties interface [App packaging and management]","GetBoolValue method","IAppxManifestProperties.GetBoolValue","IAppxManifestProperties::GetBoolValue","appxpackaging/IAppxManifestProperties::GetBoolValue","appxpkg.iappxmanifestproperties_getboolvalue"]
old-location: appxpkg\iappxmanifestproperties_getboolvalue.htm
tech.root: appxpkg
ms.assetid: 228FD28A-E65E-484B-81EF-83CC993F05D6
ms.date: 12/05/2018
ms.keywords: GetBoolValue, GetBoolValue method [App packaging and management], GetBoolValue method [App packaging and management],IAppxManifestProperties interface, IAppxManifestProperties interface [App packaging and management],GetBoolValue method, IAppxManifestProperties.GetBoolValue, IAppxManifestProperties::GetBoolValue, appxpackaging/IAppxManifestProperties::GetBoolValue, appxpkg.iappxmanifestproperties_getboolvalue
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
 - IAppxManifestProperties::GetBoolValue
 - appxpackaging/IAppxManifestProperties::GetBoolValue
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
 - IAppxManifestProperties.GetBoolValue
---

# IAppxManifestProperties::GetBoolValue


## -description

Gets the value of the specified Boolean element in the properties section.

## -parameters

### -param name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The name of the Boolean element. Valid values include:

<p class="indent">"Framework"

<p class="indent">"ResourcePackage" for Windows 8.1 and later

### -param value [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

The value of the specified Boolean element.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If a valid Boolean property with this name is not defined in the manifest, this method  returns <b>E_INVALIDARG</b> and <i>value</i> is <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestproperties">IAppxManifestProperties</a>