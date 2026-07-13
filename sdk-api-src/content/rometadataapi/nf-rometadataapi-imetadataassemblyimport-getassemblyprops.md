---
UID: NF:rometadataapi.IMetaDataAssemblyImport.GetAssemblyProps
title: IMetaDataAssemblyImport::GetAssemblyProps (rometadataapi.h)
description: Gets the set of properties for the assembly with the specified metadata signature.
helpviewer_keywords: ["GetAssemblyProps","GetAssemblyProps method [Windows Runtime]","GetAssemblyProps method [Windows Runtime]","IMetaDataAssemblyImport interface","IMetaDataAssemblyImport interface [Windows Runtime]","GetAssemblyProps method","IMetaDataAssemblyImport.GetAssemblyProps","IMetaDataAssemblyImport::GetAssemblyProps","rometadataapi/IMetaDataAssemblyImport::GetAssemblyProps","winrt.imetadataassemblyimport_getassemblyprops"]
old-location: winrt\imetadataassemblyimport_getassemblyprops.htm
tech.root: WinRT
ms.assetid: 1f60657c-46b4-4491-a9e2-73868886f51d
ms.date: 12/05/2018
ms.keywords: GetAssemblyProps, GetAssemblyProps method [Windows Runtime], GetAssemblyProps method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],GetAssemblyProps method, IMetaDataAssemblyImport.GetAssemblyProps, IMetaDataAssemblyImport::GetAssemblyProps, rometadataapi/IMetaDataAssemblyImport::GetAssemblyProps, winrt.imetadataassemblyimport_getassemblyprops
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
 - IMetaDataAssemblyImport::GetAssemblyProps
 - rometadataapi/IMetaDataAssemblyImport::GetAssemblyProps
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
 - IMetaDataAssemblyImport.GetAssemblyProps
---

# IMetaDataAssemblyImport::GetAssemblyProps


## -description

Gets the set of properties for the assembly with the specified metadata signature.

## -parameters

### -param mda [in]

The <b>mdAssembly</b> metadata token that represents the assembly for which to get the properties.

### -param ppbPublicKey [out]

A pointer to the public key or the metadata token.

### -param pcbPublicKey [out]

The number of bytes in the returned public key.

### -param pulHashAlgId [out]

A pointer to the algorithm used to hash the files in the assembly.

### -param szName [out]

The simple name of the assembly.

### -param cchName [in]

The size, in wide chars, of <i>szName</i>.

### -param pchName [out]

The number of wide chars actually returned in <i>szName</i>.

### -param pMetaData [out]

A pointer to an <a href="/dotnet/framework/unmanaged-api/metadata/assemblymetadata-structure">ASSEMBLYMETADATA</a> structure that contains the assembly metadata.

### -param pdwAssemblyFlags [out]

Flags that describe the metadata applied to an assembly. This value is a combination of one or more <a href="/dotnet/framework/unmanaged-api/metadata/corassemblyflags-enumeration">CorAssemblyFlags</a> values.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport">IMetaDataAssemblyImport</a>