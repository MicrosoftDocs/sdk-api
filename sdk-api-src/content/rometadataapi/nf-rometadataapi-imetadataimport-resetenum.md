---
UID: NF:rometadataapi.IMetaDataImport.ResetEnum
title: IMetaDataImport::ResetEnum (rometadataapi.h)
description: Resets the specified enumerator to the specified position.
helpviewer_keywords: ["IMetaDataImport interface [Windows Runtime]","ResetEnum method","IMetaDataImport.ResetEnum","IMetaDataImport::ResetEnum","ResetEnum","ResetEnum method [Windows Runtime]","ResetEnum method [Windows Runtime]","IMetaDataImport interface","rometadataapi/IMetaDataImport::ResetEnum","winrt.imetadataimport_resetenum"]
old-location: winrt\imetadataimport_resetenum.htm
tech.root: WinRT
ms.assetid: 74168393-e2ec-44bb-9fae-2c76ad40a3f8
ms.date: 12/05/2018
ms.keywords: IMetaDataImport interface [Windows Runtime],ResetEnum method, IMetaDataImport.ResetEnum, IMetaDataImport::ResetEnum, ResetEnum, ResetEnum method [Windows Runtime], ResetEnum method [Windows Runtime],IMetaDataImport interface, rometadataapi/IMetaDataImport::ResetEnum, winrt.imetadataimport_resetenum
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
 - IMetaDataImport::ResetEnum
 - rometadataapi/IMetaDataImport::ResetEnum
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
 - IMetaDataImport.ResetEnum
---

# IMetaDataImport::ResetEnum


## -description

Resets the specified enumerator to the specified position.

## -parameters

### -param hEnum [in]

The enumerator to reset.

### -param ulPos [in]

The new position at which to place the enumerator.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>