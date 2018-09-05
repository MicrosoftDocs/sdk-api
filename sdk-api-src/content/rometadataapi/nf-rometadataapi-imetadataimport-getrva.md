---
UID: NF:rometadataapi.IMetaDataImport.GetRVA
title: IMetaDataImport::GetRVA
author: windows-sdk-content
description: Gets the relative virtual address (RVA) and the implementation flags of the method or field represented by the specified token.
old-location: winrt\imetadataimport_getrva.htm
old-project: WinRT
ms.assetid: 125f7891-0ffe-48f9-a9de-4b4d2f50fc25
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetRVA, GetRVA method [Windows Runtime], GetRVA method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetRVA method, IMetaDataImport.GetRVA, IMetaDataImport::GetRVA, rometadataapi/IMetaDataImport::GetRVA, winrt.imetadataimport_getrva
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rometadataapi.h
req.include-header: 
req.redist: 
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
 - IMetaDataImport.GetRVA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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

A pointer to the implementation flags for the method. This value is a bitmask from the <a href="http://msdn.microsoft.com/en-us/library/ms233456.aspx">CorMethodImpl</a> enumeration. The value of <i>pdwImplFlags</i> is valid only if <i>tk</i> is a MethodDef token.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

