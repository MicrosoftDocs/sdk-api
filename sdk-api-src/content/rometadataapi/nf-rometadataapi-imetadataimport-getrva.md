---
UID: NF:rometadataapi.IMetaDataImport.GetRVA
title: IMetaDataImport::GetRVA (rometadataapi.h)
author: windows-sdk-content
description: Gets the relative virtual address (RVA) and the implementation flags of the method or field represented by the specified token.
old-location: winrt\imetadataimport_getrva.htm
tech.root: WinRT
ms.assetid: 125f7891-0ffe-48f9-a9de-4b4d2f50fc25
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRVA, GetRVA method [Windows Runtime], GetRVA method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetRVA method, IMetaDataImport.GetRVA, IMetaDataImport::GetRVA, rometadataapi/IMetaDataImport::GetRVA, winrt.imetadataimport_getrva
ms.topic: method
f1_keywords: 
 - "rometadataapi/IMetaDataImport.GetRVA"
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
 - IMetaDataImport.GetRVA
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataImport::GetRVA


## -description


Gets the relative virtual address (RVA) and the implementation flags of the method or field represented by the specified token.


## -parameters




### -param tk [in]

A MethodDef or FieldDef metadata token that represents the code object to return the RVA for. If the token is a FieldDef, the field must be a global variable.


### -param pulCodeRVA [out]

 A pointer to the relative virtual address of the code object represented by the token.


### -param pdwImplFlags [out]

A pointer to the implementation flags for the method. This value is a bitmask from the <a href="https://docs.microsoft.com/dotnet/framework/unmanaged-api/metadata/cormethodimpl-enumeration">CorMethodImpl</a> enumeration. The value of <i>pdwImplFlags</i> is valid only if <i>tk</i> is a MethodDef token.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>
 

 

