---
UID: NF:rometadataapi.IMetaDataImport.GetModuleRefProps
title: IMetaDataImport::GetModuleRefProps (rometadataapi.h)
description: Gets the name of the module referenced by the specified metadata token.
helpviewer_keywords: ["GetModuleRefProps","GetModuleRefProps method [Windows Runtime]","GetModuleRefProps method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetModuleRefProps method","IMetaDataImport.GetModuleRefProps","IMetaDataImport::GetModuleRefProps","rometadataapi/IMetaDataImport::GetModuleRefProps","winrt.imetadataimport_getmodulerefprops"]
old-location: winrt\imetadataimport_getmodulerefprops.htm
tech.root: WinRT
ms.assetid: 1f14fe81-d585-4167-8817-0c7d000413de
ms.date: 12/05/2018
ms.keywords: GetModuleRefProps, GetModuleRefProps method [Windows Runtime], GetModuleRefProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetModuleRefProps method, IMetaDataImport.GetModuleRefProps, IMetaDataImport::GetModuleRefProps, rometadataapi/IMetaDataImport::GetModuleRefProps, winrt.imetadataimport_getmodulerefprops
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
 - IMetaDataImport::GetModuleRefProps
 - rometadataapi/IMetaDataImport::GetModuleRefProps
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
 - IMetaDataImport.GetModuleRefProps
---

# IMetaDataImport::GetModuleRefProps


## -description

Gets the name of the module referenced by the specified metadata token.

## -parameters

### -param tkModuleRef [in]

The ModuleRef metadata token that references the module to get metadata information for.

### -param szName [out]

A buffer to hold the module name.

### -param cchName [in]

The requested size of <i>szName</i> in wide characters.

### -param pchName [out]

The returned size of <i>szName</i> in wide characters.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>