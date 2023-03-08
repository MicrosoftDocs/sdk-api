---
UID: NF:rometadataapi.IMetaDataImport.CountEnum
title: IMetaDataImport::CountEnum (rometadataapi.h)
description: Gets the number of elements in the enumeration that was retrieved by the specified enumerator.
helpviewer_keywords: ["CountEnum","CountEnum method [Windows Runtime]","CountEnum method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","CountEnum method","IMetaDataImport.CountEnum","IMetaDataImport::CountEnum","rometadataapi/IMetaDataImport::CountEnum","winrt.imetadataimport_countenum"]
old-location: winrt\imetadataimport_countenum.htm
tech.root: WinRT
ms.assetid: 67146070-1710-4602-845c-a2a3cd5efdad
ms.date: 12/05/2018
ms.keywords: CountEnum, CountEnum method [Windows Runtime], CountEnum method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],CountEnum method, IMetaDataImport.CountEnum, IMetaDataImport::CountEnum, rometadataapi/IMetaDataImport::CountEnum, winrt.imetadataimport_countenum
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
 - IMetaDataImport::CountEnum
 - rometadataapi/IMetaDataImport::CountEnum
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
 - IMetaDataImport.CountEnum
---

# IMetaDataImport::CountEnum


## -description

Gets the number of elements in the enumeration that was retrieved by the specified enumerator.

## -parameters

### -param hEnum [in]

The handle for the enumerator.

### -param pulCount [out, retval]

The number of elements enumerated.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The handle specified by <i>hEnum</i> is obtained from a previous <b>Enum</b><i>Name</i> call (for example, <a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumtypedefs">IMetaDataImport::EnumTypeDefs</a>).

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>