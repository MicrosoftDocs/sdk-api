---
UID: NF:rometadataapi.IMetaDataImport.GetModuleFromScope
title: IMetaDataImport::GetModuleFromScope (rometadataapi.h)
description: Gets a metadata token for the module referenced in the current metadata scope.
helpviewer_keywords: ["GetModuleFromScope","GetModuleFromScope method [Windows Runtime]","GetModuleFromScope method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetModuleFromScope method","IMetaDataImport.GetModuleFromScope","IMetaDataImport::GetModuleFromScope","rometadataapi/IMetaDataImport::GetModuleFromScope","winrt.imetadataimport_getmodulefromscope"]
old-location: winrt\imetadataimport_getmodulefromscope.htm
tech.root: WinRT
ms.assetid: 4ad7248d-7266-4a14-b499-05bda7f60e01
ms.date: 12/05/2018
ms.keywords: GetModuleFromScope, GetModuleFromScope method [Windows Runtime], GetModuleFromScope method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetModuleFromScope method, IMetaDataImport.GetModuleFromScope, IMetaDataImport::GetModuleFromScope, rometadataapi/IMetaDataImport::GetModuleFromScope, winrt.imetadataimport_getmodulefromscope
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
 - IMetaDataImport::GetModuleFromScope
 - rometadataapi/IMetaDataImport::GetModuleFromScope
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
 - IMetaDataImport.GetModuleFromScope
---

# IMetaDataImport::GetModuleFromScope


## -description

Gets a metadata token for the module referenced in the current metadata scope.

## -parameters

### -param ptkModule [out]

 A pointer to the token representing the module referenced in the current metadata scope.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>