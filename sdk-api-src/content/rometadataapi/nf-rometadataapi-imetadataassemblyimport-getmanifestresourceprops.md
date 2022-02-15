---
UID: NF:rometadataapi.IMetaDataAssemblyImport.GetManifestResourceProps
title: IMetaDataAssemblyImport::GetManifestResourceProps (rometadataapi.h)
description: Gets the set of properties of the manifest resource with the specified metadata signature.
helpviewer_keywords: ["GetManifestResourceProps","GetManifestResourceProps method [Windows Runtime]","GetManifestResourceProps method [Windows Runtime]","IMetaDataAssemblyImport interface","IMetaDataAssemblyImport interface [Windows Runtime]","GetManifestResourceProps method","IMetaDataAssemblyImport.GetManifestResourceProps","IMetaDataAssemblyImport::GetManifestResourceProps","rometadataapi/IMetaDataAssemblyImport::GetManifestResourceProps","winrt.imetadataassemblyimport_getmanifestresourceprops"]
old-location: winrt\imetadataassemblyimport_getmanifestresourceprops.htm
tech.root: WinRT
ms.assetid: caa859c8-de40-4de6-bf90-41104cef91b2
ms.date: 12/05/2018
ms.keywords: GetManifestResourceProps, GetManifestResourceProps method [Windows Runtime], GetManifestResourceProps method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],GetManifestResourceProps method, IMetaDataAssemblyImport.GetManifestResourceProps, IMetaDataAssemblyImport::GetManifestResourceProps, rometadataapi/IMetaDataAssemblyImport::GetManifestResourceProps, winrt.imetadataassemblyimport_getmanifestresourceprops
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
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
 - IMetaDataAssemblyImport::GetManifestResourceProps
 - rometadataapi/IMetaDataAssemblyImport::GetManifestResourceProps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataAssemblyImport.GetManifestResourceProps
---

# IMetaDataAssemblyImport::GetManifestResourceProps


## -description

Gets the set of properties of the manifest resource with the specified metadata signature.

## -parameters

### -param mdmr [in]

An <b>mdManifestResource</b> token that represents the resource for which to get the properties.

### -param szName [out]

The name of the resource.

### -param cchName [in]

The size, in wide chars, of <i>szName</i>.

### -param pchName [out]

A pointer to the number of wide chars actually returned in <i>szName</i>.

### -param ptkImplementation [out]

A pointer to an <b>mdFile</b> token or an <b>mdAssemblyRef</b> token that represents the file or assembly, respectively, that contains the resource.

### -param pdwOffset [out]

A pointer to a value that specifies the offset to the beginning of the resource within the file.

### -param pdwResourceFlags [out]

A pointer to flags that describe the metadata applied to a resource. The flags value is a combination of one or more <a href="/dotnet/framework/unmanaged-api/metadata/cormanifestresourceflags-enumeration">CorManifestResourceFlags</a> values.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport">IMetaDataAssemblyImport</a>