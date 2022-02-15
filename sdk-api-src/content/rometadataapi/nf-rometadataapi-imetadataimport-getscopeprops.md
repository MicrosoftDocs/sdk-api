---
UID: NF:rometadataapi.IMetaDataImport.GetScopeProps
title: IMetaDataImport::GetScopeProps (rometadataapi.h)
description: Gets the name and optionally the version identifier of the assembly or module in the current metadata scope.
helpviewer_keywords: ["GetScopeProps","GetScopeProps method [Windows Runtime]","GetScopeProps method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetScopeProps method","IMetaDataImport.GetScopeProps","IMetaDataImport::GetScopeProps","rometadataapi/IMetaDataImport::GetScopeProps","winrt.imetadataimport_getscopeprops"]
old-location: winrt\imetadataimport_getscopeprops.htm
tech.root: WinRT
ms.assetid: e7c7cc92-fa0e-426d-b26d-d8f87bffad7d
ms.date: 12/05/2018
ms.keywords: GetScopeProps, GetScopeProps method [Windows Runtime], GetScopeProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetScopeProps method, IMetaDataImport.GetScopeProps, IMetaDataImport::GetScopeProps, rometadataapi/IMetaDataImport::GetScopeProps, winrt.imetadataimport_getscopeprops
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
 - IMetaDataImport::GetScopeProps
 - rometadataapi/IMetaDataImport::GetScopeProps
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
 - IMetaDataImport.GetScopeProps
---

# IMetaDataImport::GetScopeProps


## -description

Gets the name and optionally the version identifier of the assembly or module in the current metadata scope.

## -parameters

### -param szName [out]

A buffer for the assembly or module name.

### -param cchName [in]

The size in wide characters of <i>szName</i>.

### -param pchName [out]

The number of wide characters returned in <i>szName</i>.

### -param pmvid [out]

A pointer to a GUID that uniquely identifies the version of the assembly or module.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>