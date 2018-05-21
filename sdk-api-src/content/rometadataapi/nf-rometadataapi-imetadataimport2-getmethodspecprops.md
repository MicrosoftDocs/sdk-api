---
UID: NF:rometadataapi.IMetaDataImport2.GetMethodSpecProps
title: IMetaDataImport2::GetMethodSpecProps
author: windows-driver-content
description: Gets the metadata signature of the method referenced by the specified MethodSpec token.
old-location: winrt\imetadataimport2_getmethodspecprops.htm
old-project: WinRT
ms.assetid: 498ee212-000d-4204-ae7a-de553bf3ea45
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: GetMethodSpecProps, GetMethodSpecProps method [Windows Runtime], GetMethodSpecProps method [Windows Runtime],IMetaDataImport2 interface, IMetaDataImport2 interface [Windows Runtime],GetMethodSpecProps method, IMetaDataImport2.GetMethodSpecProps, IMetaDataImport2::GetMethodSpecProps, rometadataapi/IMetaDataImport2::GetMethodSpecProps, winrt.imetadataimport2_getmethodspecprops
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
-	IMetaDataImport2.GetMethodSpecProps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMetaDataImport2::GetMethodSpecProps


## -description


Gets the metadata signature of the method referenced by the specified MethodSpec token.


## -parameters




### -param mi [in]

A <b>MethodSpec</b> token that represents the instantiation of the method.


### -param tkParent [out]

A pointer to the <b>MethodDef</b> or <b>MethodRef</b> token that represents the method definition.




### -param ppvSigBlob [out]

 A pointer to the binary metadata signature of the method.


### -param pcbSigBlob [out]

The size, in bytes, of <i>ppvSigBlob</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/32c462e0-d4b8-44db-b24b-c86b46be85bf">IMetaDataImport2</a>
 

 

