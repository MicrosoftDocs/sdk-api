---
UID: NF:rometadataapi.IMetaDataAssemblyImport.GetAssemblyRefProps
title: IMetaDataAssemblyImport::GetAssemblyRefProps
author: windows-sdk-content
description: Gets the set of properties for the assembly reference with the specified metadata signature.
old-location: winrt\imetadataassemblyimport_getassemblyrefprops.htm
old-project: WinRT
ms.assetid: b2a0d54f-dc9d-4c3c-80e7-725da985f23b
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetAssemblyRefProps, GetAssemblyRefProps method [Windows Runtime], GetAssemblyRefProps method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],GetAssemblyRefProps method, IMetaDataAssemblyImport.GetAssemblyRefProps, IMetaDataAssemblyImport::GetAssemblyRefProps, rometadataapi/IMetaDataAssemblyImport::GetAssemblyRefProps, winrt.imetadataassemblyimport_getassemblyrefprops
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataAssemblyImport.GetAssemblyRefProps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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

A pointer to an <a href="http://msdn.microsoft.com/en-us/library/ms230277.aspx">ASSEMBLYMETADATA</a> structure that contains the assembly metadata.


### -param ppbHashValue [out]

A pointer to the hash value. This is the hash, using the SHA-1 algorithm, of the PublicKey property of the assembly being referenced, unless the arfFullOriginator flag of the <a href="http://msdn.microsoft.com/en-us/library/ms232921.aspx">AssemblyRefFlags</a> enumeration is set.




### -param pcbHashValue [out]

The number of wide chars in the returned hash value.


### -param pdwAssemblyRefFlags [out]

 A pointer to flags that describe the metadata applied to an assembly. The flags value is a combination of one or more <a href="http://msdn.microsoft.com/en-us/library/ms232517.aspx">CorAssemblyFlags</a> values.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c4ae6028-87ac-4bb9-8eda-c6a48e5ecd3c">IMetaDataAssemblyImport</a>
 

 

