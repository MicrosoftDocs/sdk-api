---
UID: NF:rometadataapi.IMetaDataImport.GetMethodProps
title: IMetaDataImport::GetMethodProps
author: windows-driver-content
description: Gets the metadata associated with the method referenced by the specified MethodDef token.
old-location: winrt\imetadataimport_getmethodprops.htm
old-project: WinRT
ms.assetid: 973f2a8c-025d-4d27-ac99-56902b1132dd
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: GetMethodProps, GetMethodProps method [Windows Runtime], GetMethodProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetMethodProps method, IMetaDataImport.GetMethodProps, IMetaDataImport::GetMethodProps, rometadataapi/IMetaDataImport::GetMethodProps, winrt.imetadataimport_getmethodprops
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	rometadataapi.h
api_name:
-	IMetaDataImport.GetMethodProps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMetaDataImport::GetMethodProps


## -description


Gets the metadata associated with the method referenced by the specified MethodDef token.


## -parameters




### -param tkMethodDef [in]

The MethodDef token that represents the method to return metadata for.


### -param ptkClass [out]

A Pointer to a TypeDef token that represents the type that implements the method.


### -param szMethod [out]

A Pointer to a buffer that has the method's name.


### -param cchMethod [in]

The requested size of <i>szMethod</i>.


### -param pchMethod [out]

A pointer to the size in wide characters of <i>szMethod</i>, or in the case of truncation, the actual number of wide characters in the method name.


### -param pdwAttr [out]

A pointer to any flags associated with the method.


### -param ppvSigBlob [out]

A pointer to the binary metadata signature of the method.


### -param pcbSigBlob [out]

A pointer to the size in bytes of <i>ppvSigBlob</i>.


### -param pulCodeRVA [out]

A pointer to the relative virtual address of the method.


### -param pdwImplFlags [out]

A pointer to any implementation flags for the method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

