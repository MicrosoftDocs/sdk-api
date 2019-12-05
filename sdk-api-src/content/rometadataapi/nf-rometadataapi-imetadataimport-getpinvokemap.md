---
UID: NF:rometadataapi.IMetaDataImport.GetPinvokeMap
title: IMetaDataImport::GetPinvokeMap (rometadataapi.h)
description: Gets a ModuleRef token to represent the target assembly of a PInvoke call.
old-location: winrt\imetadataimport_getpinvokemap.htm
tech.root: WinRT
ms.assetid: bf83785d-ba4f-4a11-84ee-92d010c8a1fc
ms.date: 12/05/2018
ms.keywords: GetPinvokeMap, GetPinvokeMap method [Windows Runtime], GetPinvokeMap method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetPinvokeMap method, IMetaDataImport.GetPinvokeMap, IMetaDataImport::GetPinvokeMap, rometadataapi/IMetaDataImport::GetPinvokeMap, winrt.imetadataimport_getpinvokemap
ms.topic: method
f1_keywords:
- rometadataapi/IMetaDataImport.GetPinvokeMap
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
- IMetaDataImport.GetPinvokeMap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataImport::GetPinvokeMap


## -description


Gets a ModuleRef token to represent the target assembly of a PInvoke call.


## -parameters




### -param tk [in]

A FieldDef or MethodDef token to get the PInvoke mapping metadata for.


### -param pdwMappingFlags [out]

A pointer to flags used for mapping. This value is a bitmask from the <a href="https://docs.microsoft.com/dotnet/framework/unmanaged-api/metadata/corpinvokemap-enumeration">CorPinvokeMap</a> enumeration.


### -param szImportName [out]

The name of the unmanaged target DLL.


### -param cchImportName [in]

The size in wide characters of <i>szImportName</i>.


### -param pchImportName [out]

The number of wide characters returned in <i>szImportName</i>.


### -param ptkImportDLL [out]

A pointer to a ModuleRef token that represents the unmanaged target object library.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>
 

 

