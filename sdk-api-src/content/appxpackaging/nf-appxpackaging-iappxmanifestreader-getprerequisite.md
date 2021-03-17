---
UID: NF:appxpackaging.IAppxManifestReader.GetPrerequisite
title: IAppxManifestReader::GetPrerequisite (appxpackaging.h)
description: Gets the specified prerequisite as defined in the package manifest.
helpviewer_keywords: ["GetPrerequisite","GetPrerequisite method [App packaging and management]","GetPrerequisite method [App packaging and management]","IAppxManifestReader interface","IAppxManifestReader interface [App packaging and management]","GetPrerequisite method","IAppxManifestReader.GetPrerequisite","IAppxManifestReader::GetPrerequisite","appxpackaging/IAppxManifestReader::GetPrerequisite","appxpkg.iappxmanifestreader_getprerequisite"]
old-location: appxpkg\iappxmanifestreader_getprerequisite.htm
tech.root: appxpkg
ms.assetid: 1CF44513-AA07-4591-9134-A156A538C8F1
ms.date: 12/05/2018
ms.keywords: GetPrerequisite, GetPrerequisite method [App packaging and management], GetPrerequisite method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetPrerequisite method, IAppxManifestReader.GetPrerequisite, IAppxManifestReader::GetPrerequisite, appxpackaging/IAppxManifestReader::GetPrerequisite, appxpkg.iappxmanifestreader_getprerequisite
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
 - IAppxManifestReader::GetPrerequisite
 - appxpackaging/IAppxManifestReader::GetPrerequisite
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
 - IAppxManifestReader.GetPrerequisite
---

# IAppxManifestReader::GetPrerequisite


## -description

Gets the specified prerequisite as defined in the package manifest.

## -parameters

### -param name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The name of the prerequisite, either "OSMinVersion" or "OSMaxVersionTested".

### -param value [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a>*</b>

The specified prerequisite. In the manifest the dot-trio representation is Major.Minor.AppPlatform. This is converted to the 64-bit value as the follows:
The highest order word contains the Major version. The next word contains the Minor version.	The next word contains the optional AppPlatform version, if specified.

## -returns

Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The prerequisite defined in <i>name</i> is not defined in the manifest.

</td>
</tr>
</table>

## -remarks

Prerequisites are specified using the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-osminversion">OSMinVersion</a> and <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-osmaxversiontested">OSMaxVersionTested</a> elements in the package manifest.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>