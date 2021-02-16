---
UID: NF:rometadataapi.IMetaDataImport.IsValidToken
title: IMetaDataImport::IsValidToken (rometadataapi.h)
description: Gets a value indicating whether the specified token holds a valid reference to a code object.
helpviewer_keywords: ["IMetaDataImport interface [Windows Runtime]","IsValidToken method","IMetaDataImport.IsValidToken","IMetaDataImport::IsValidToken","IsValidToken","IsValidToken method [Windows Runtime]","IsValidToken method [Windows Runtime]","IMetaDataImport interface","rometadataapi/IMetaDataImport::IsValidToken","winrt.imetadataimport_isvalidtoken"]
old-location: winrt\imetadataimport_isvalidtoken.htm
tech.root: WinRT
ms.assetid: 9829a600-38fb-48ac-a486-abb56d17afdf
ms.date: 12/05/2018
ms.keywords: IMetaDataImport interface [Windows Runtime],IsValidToken method, IMetaDataImport.IsValidToken, IMetaDataImport::IsValidToken, IsValidToken, IsValidToken method [Windows Runtime], IsValidToken method [Windows Runtime],IMetaDataImport interface, rometadataapi/IMetaDataImport::IsValidToken, winrt.imetadataimport_isvalidtoken
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
 - IMetaDataImport::IsValidToken
 - rometadataapi/IMetaDataImport::IsValidToken
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
 - IMetaDataImport.IsValidToken
---

# IMetaDataImport::IsValidToken


## -description

Gets a value indicating whether the specified token holds a valid reference to a code object.

## -parameters

### -param tk [in]

The token to check the reference validity for.

## -returns

<b>true</b> if <i>tk</i> is a valid metadata token within the current scope. Otherwise, <b>false</b>.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>