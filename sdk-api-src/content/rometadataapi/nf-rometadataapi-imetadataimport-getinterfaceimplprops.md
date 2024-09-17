---
UID: NF:rometadataapi.IMetaDataImport.GetInterfaceImplProps
title: IMetaDataImport::GetInterfaceImplProps (rometadataapi.h)
description: Gets a pointer to the metadata tokens for the Type that implements the specified method, and for the interface that declares that method.
helpviewer_keywords: ["GetInterfaceImplProps","GetInterfaceImplProps method [Windows Runtime]","GetInterfaceImplProps method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetInterfaceImplProps method","IMetaDataImport.GetInterfaceImplProps","IMetaDataImport::GetInterfaceImplProps","rometadataapi/IMetaDataImport::GetInterfaceImplProps","winrt.imetadataimport_getinterfaceimplprops"]
old-location: winrt\imetadataimport_getinterfaceimplprops.htm
tech.root: WinRT
ms.assetid: ff91bb07-8e3a-49f1-9cd6-1c3e18a3c242
ms.date: 12/05/2018
ms.keywords: GetInterfaceImplProps, GetInterfaceImplProps method [Windows Runtime], GetInterfaceImplProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetInterfaceImplProps method, IMetaDataImport.GetInterfaceImplProps, IMetaDataImport::GetInterfaceImplProps, rometadataapi/IMetaDataImport::GetInterfaceImplProps, winrt.imetadataimport_getinterfaceimplprops
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
 - IMetaDataImport::GetInterfaceImplProps
 - rometadataapi/IMetaDataImport::GetInterfaceImplProps
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
 - IMetaDataImport.GetInterfaceImplProps
---

# IMetaDataImport::GetInterfaceImplProps


## -description

Gets a pointer to the metadata tokens for the implementater-implementee relationship between two types.

## -parameters

### -param tkInterfaceImpl [in]

The metadata token representing the interface implementation relationship.

### -param ptkClass [out]

The metadata token representing the implementer: the class or interface that implements the interface <b>ptkIface</b>.

### -param ptkIface [out]

The metadata token representing the implementee: the interface that is implemented by <b>ptkClass</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>InterfaceImpl</b> token represents one of the n:1 relationships between an implementee and the implementer.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>
