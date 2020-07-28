---
UID: NF:rometadataapi.IMetaDataImport.GetTypeSpecFromToken
title: IMetaDataImport::GetTypeSpecFromToken (rometadataapi.h)
description: Gets the binary metadata signature of the type specification represented by the specified token.
helpviewer_keywords: ["GetTypeSpecFromToken","GetTypeSpecFromToken method [Windows Runtime]","GetTypeSpecFromToken method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetTypeSpecFromToken method","IMetaDataImport.GetTypeSpecFromToken","IMetaDataImport::GetTypeSpecFromToken","rometadataapi/IMetaDataImport::GetTypeSpecFromToken","winrt.imetadataimport_gettypespecfromtoken"]
old-location: winrt\imetadataimport_gettypespecfromtoken.htm
tech.root: WinRT
ms.assetid: e03b6c5f-c68a-44a9-a203-8ed00293b582
ms.date: 12/05/2018
ms.keywords: GetTypeSpecFromToken, GetTypeSpecFromToken method [Windows Runtime], GetTypeSpecFromToken method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetTypeSpecFromToken method, IMetaDataImport.GetTypeSpecFromToken, IMetaDataImport::GetTypeSpecFromToken, rometadataapi/IMetaDataImport::GetTypeSpecFromToken, winrt.imetadataimport_gettypespecfromtoken
f1_keywords:
- rometadataapi/IMetaDataImport.GetTypeSpecFromToken
dev_langs:
- c++
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
- IMetaDataImport.GetTypeSpecFromToken
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataImport::GetTypeSpecFromToken


## -description


Gets the binary metadata signature of the type specification represented by the specified token.


## -parameters




### -param tkTypeSpec [in]

The TypeSpec token associated with the requested metadata signature.


### -param ppvSig [out]

 A pointer to the binary metadata signature.


### -param pcbSig [out]

The size, in bytes, of the metadata signature.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>
 

 

