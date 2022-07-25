---
UID: NF:rometadataapi.IMetaDataImport.GetSigFromToken
title: IMetaDataImport::GetSigFromToken (rometadataapi.h)
description: Gets the binary metadata signature associated with the specified token.
helpviewer_keywords: ["GetSigFromToken","GetSigFromToken method [Windows Runtime]","GetSigFromToken method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetSigFromToken method","IMetaDataImport.GetSigFromToken","IMetaDataImport::GetSigFromToken","rometadataapi/IMetaDataImport::GetSigFromToken","winrt.imetadataimport_getsigfromtoken"]
old-location: winrt\imetadataimport_getsigfromtoken.htm
tech.root: WinRT
ms.assetid: babd95ef-7786-47da-b5f6-c1fef93a4504
ms.date: 12/05/2018
ms.keywords: GetSigFromToken, GetSigFromToken method [Windows Runtime], GetSigFromToken method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetSigFromToken method, IMetaDataImport.GetSigFromToken, IMetaDataImport::GetSigFromToken, rometadataapi/IMetaDataImport::GetSigFromToken, winrt.imetadataimport_getsigfromtoken
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
 - IMetaDataImport::GetSigFromToken
 - rometadataapi/IMetaDataImport::GetSigFromToken
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
 - IMetaDataImport.GetSigFromToken
---

# IMetaDataImport::GetSigFromToken


## -description

Gets the binary metadata signature associated with the specified token.

## -parameters

### -param tkSignature [in]

The token to return the binary metadata signature for.

### -param ppvSig [out]

A pointer to the returned metadata signature.

### -param pcbSig [out]

The size in bytes of the binary metadata signature.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>