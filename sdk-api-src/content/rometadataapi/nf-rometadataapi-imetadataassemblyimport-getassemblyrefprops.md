---
UID: NF:rometadataapi.IMetaDataAssemblyImport.GetAssemblyRefProps
title: IMetaDataAssemblyImport::GetAssemblyRefProps (rometadataapi.h)
description: Gets the set of properties for the assembly reference with the specified metadata signature.
helpviewer_keywords: ["GetAssemblyRefProps","GetAssemblyRefProps method [Windows Runtime]","GetAssemblyRefProps method [Windows Runtime]","IMetaDataAssemblyImport interface","IMetaDataAssemblyImport interface [Windows Runtime]","GetAssemblyRefProps method","IMetaDataAssemblyImport.GetAssemblyRefProps","IMetaDataAssemblyImport::GetAssemblyRefProps","rometadataapi/IMetaDataAssemblyImport::GetAssemblyRefProps","winrt.imetadataassemblyimport_getassemblyrefprops"]
old-location: winrt\imetadataassemblyimport_getassemblyrefprops.htm
tech.root: WinRT
ms.assetid: b2a0d54f-dc9d-4c3c-80e7-725da985f23b
ms.date: 12/05/2018
ms.keywords: GetAssemblyRefProps, GetAssemblyRefProps method [Windows Runtime], GetAssemblyRefProps method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],GetAssemblyRefProps method, IMetaDataAssemblyImport.GetAssemblyRefProps, IMetaDataAssemblyImport::GetAssemblyRefProps, rometadataapi/IMetaDataAssemblyImport::GetAssemblyRefProps, winrt.imetadataassemblyimport_getassemblyrefprops
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
 - IMetaDataAssemblyImport::GetAssemblyRefProps
 - rometadataapi/IMetaDataAssemblyImport::GetAssemblyRefProps
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
 - IMetaDataAssemblyImport.GetAssemblyRefProps
---

# IMetaDataAssemblyImport::GetAssemblyRefProps


## -description

Gets the set of properties for the assembly reference with the specified metadata signature.

## -parameters

### -param mdar [in]

The <b>mdAssemblyRef</b> metadata token that represents the assembly reference for which to get the properties.

### -param ppbPublicKeyOrToken [out]

A pointer to the public key or the metadata token.

### -param pcbPublicKeyOrToken [out]

The number of bytes in the returned public key or token.

### -param szName [out]

The simple name of the assembly.

### -param cchName [in]

The size, in wide chars, of <i>szName</i>.

### -param pchName [out]

A  pointer to the number of wide chars actually returned in <i>szName</i>.

### -param pMetaData [out]

A pointer to an <a href="/dotnet/framework/unmanaged-api/metadata/assemblymetadata-structure">ASSEMBLYMETADATA</a> structure that contains the assembly metadata.

### -param ppbHashValue [out]

A pointer to the hash value. This is the hash, using the SHA-1 algorithm, of the PublicKey property of the assembly being referenced, unless the arfFullOriginator flag of the <a href="/dotnet/framework/unmanaged-api/metadata/assemblyrefflags-enumeration">AssemblyRefFlags</a> enumeration is set.

### -param pcbHashValue [out]

The number of wide chars in the returned hash value.

### -param pdwAssemblyRefFlags [out]

 A pointer to flags that describe the metadata applied to an assembly. The flags value is a combination of one or more <a href="/dotnet/framework/unmanaged-api/metadata/corassemblyflags-enumeration">CorAssemblyFlags</a> values.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport">IMetaDataAssemblyImport</a>