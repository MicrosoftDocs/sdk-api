---
UID: NF:rometadataapi.IMetaDataImport.GetFieldMarshal
title: IMetaDataImport::GetFieldMarshal (rometadataapi.h)
author: windows-sdk-content
description: Gets a pointer to the native, unmanaged type of the field represented by the specified field metadata token.
old-location: winrt\imetadataimport_getfieldmarshal.htm
tech.root: WinRT
ms.assetid: a176ce92-761f-48fd-b9e8-01990176df27
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFieldMarshal, GetFieldMarshal method [Windows Runtime], GetFieldMarshal method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetFieldMarshal method, IMetaDataImport.GetFieldMarshal, IMetaDataImport::GetFieldMarshal, rometadataapi/IMetaDataImport::GetFieldMarshal, winrt.imetadataimport_getfieldmarshal
ms.topic: method
f1_keywords: 
 - "rometadataapi/IMetaDataImport.GetFieldMarshal"
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
 - IMetaDataImport.GetFieldMarshal
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>
 

 

