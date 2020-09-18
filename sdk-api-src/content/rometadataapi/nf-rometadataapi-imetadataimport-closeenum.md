---
UID: NF:rometadataapi.IMetaDataImport.CloseEnum
title: IMetaDataImport::CloseEnum (rometadataapi.h)
description: Closes the enumerator that is identified by the specified handle.
helpviewer_keywords: ["CloseEnum","CloseEnum method [Windows Runtime]","CloseEnum method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","CloseEnum method","IMetaDataImport.CloseEnum","IMetaDataImport::CloseEnum","rometadataapi/IMetaDataImport::CloseEnum","winrt.imetadataimport_closeenum"]
old-location: winrt\imetadataimport_closeenum.htm
tech.root: WinRT
ms.assetid: 3495afdf-ca88-4967-b7b3-6320114b9c50
ms.date: 12/05/2018
ms.keywords: CloseEnum, CloseEnum method [Windows Runtime], CloseEnum method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],CloseEnum method, IMetaDataImport.CloseEnum, IMetaDataImport::CloseEnum, rometadataapi/IMetaDataImport::CloseEnum, winrt.imetadataimport_closeenum
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
 - IMetaDataImport::CloseEnum
 - rometadataapi/IMetaDataImport::CloseEnum
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
 - IMetaDataImport.CloseEnum
---

# IMetaDataImport::CloseEnum


## -description

Closes the enumerator that is identified by the specified handle.

## -parameters

### -param hEnum [in]

The handle of the enumerator to close.

## -remarks

The handle specified by <i>hEnum</i> is obtained from a previous <b>Enum</b><i>Name</i> call (for example, <a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumtypedefs">IMetaDataImport::EnumTypeDefs</a>).

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>