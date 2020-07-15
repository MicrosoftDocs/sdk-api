---
UID: NF:rometadataapi.IMetaDataAssemblyImport.FindManifestResourceByName
title: IMetaDataAssemblyImport::FindManifestResourceByName (rometadataapi.h)
description: Gets a pointer to the manifest resource with the specified name.
helpviewer_keywords: ["FindManifestResourceByName","FindManifestResourceByName method [Windows Runtime]","FindManifestResourceByName method [Windows Runtime]","IMetaDataAssemblyImport interface","IMetaDataAssemblyImport interface [Windows Runtime]","FindManifestResourceByName method","IMetaDataAssemblyImport.FindManifestResourceByName","IMetaDataAssemblyImport::FindManifestResourceByName","rometadataapi/IMetaDataAssemblyImport::FindManifestResourceByName","winrt.imetadataassemblyimport_findmanifestresourcebyname"]
old-location: winrt\imetadataassemblyimport_findmanifestresourcebyname.htm
tech.root: WinRT
ms.assetid: a72e4c1f-505d-4672-8baa-fbe2243b8ca0
ms.date: 12/05/2018
ms.keywords: FindManifestResourceByName, FindManifestResourceByName method [Windows Runtime], FindManifestResourceByName method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],FindManifestResourceByName method, IMetaDataAssemblyImport.FindManifestResourceByName, IMetaDataAssemblyImport::FindManifestResourceByName, rometadataapi/IMetaDataAssemblyImport::FindManifestResourceByName, winrt.imetadataassemblyimport_findmanifestresourcebyname
f1_keywords:
- rometadataapi/IMetaDataAssemblyImport.FindManifestResourceByName
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- rometadataapi.h
api_name:
- IMetaDataAssemblyImport.FindManifestResourceByName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataAssemblyImport::FindManifestResourceByName


## -description


Gets a pointer to the manifest resource with the specified name.




## -parameters




### -param szName [in]

The name of the resource.


### -param ptkManifestResource [out]

The array used to store the <b>mdManifestResource</b> metadata tokens, each of which represents a manifest resource.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method uses the standard rules employed by the common language runtime for resolving references.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport">IMetaDataAssemblyImport</a>
 

 

