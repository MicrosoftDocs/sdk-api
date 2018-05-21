---
UID: NF:rometadataapi.IMetaDataImport.GetFieldMarshal
title: IMetaDataImport::GetFieldMarshal
author: windows-driver-content
description: Gets a pointer to the native, unmanaged type of the field represented by the specified field metadata token.
old-location: winrt\imetadataimport_getfieldmarshal.htm
old-project: WinRT
ms.assetid: a176ce92-761f-48fd-b9e8-01990176df27
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: GetFieldMarshal, GetFieldMarshal method [Windows Runtime], GetFieldMarshal method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetFieldMarshal method, IMetaDataImport.GetFieldMarshal, IMetaDataImport::GetFieldMarshal, rometadataapi/IMetaDataImport::GetFieldMarshal, winrt.imetadataimport_getfieldmarshal
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
-	IMetaDataImport.GetFieldMarshal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMetaDataImport::GetFieldMarshal


## -description


Gets a pointer to the native, unmanaged type of the field represented by the specified field metadata token.


## -parameters




### -param tk [in]

The metadata token that represents the field to get interop marshaling information for.


### -param ppvNativeType [out]

A pointer to the metadata signature of the field's native type.


### -param pcbNativeType [out]

The size in bytes of <i>ppvNativeType</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

