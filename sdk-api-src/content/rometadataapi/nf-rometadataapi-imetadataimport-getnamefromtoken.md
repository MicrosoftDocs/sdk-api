---
UID: NF:rometadataapi.IMetaDataImport.GetNameFromToken
title: IMetaDataImport::GetNameFromToken (rometadataapi.h)
description: Gets the UTF-8 name of the object referenced by the specified metadata token. This method is obsolete.
helpviewer_keywords: ["GetNameFromToken","GetNameFromToken method [Windows Runtime]","GetNameFromToken method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetNameFromToken method","IMetaDataImport.GetNameFromToken","IMetaDataImport::GetNameFromToken","rometadataapi/IMetaDataImport::GetNameFromToken","winrt.imetadataimport_getnamefromtoken"]
old-location: winrt\imetadataimport_getnamefromtoken.htm
tech.root: WinRT
ms.assetid: 933d502a-c752-45ae-b51f-8c0a876856bc
ms.date: 12/05/2018
ms.keywords: GetNameFromToken, GetNameFromToken method [Windows Runtime], GetNameFromToken method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetNameFromToken method, IMetaDataImport.GetNameFromToken, IMetaDataImport::GetNameFromToken, rometadataapi/IMetaDataImport::GetNameFromToken, winrt.imetadataimport_getnamefromtoken
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
 - IMetaDataImport::GetNameFromToken
 - rometadataapi/IMetaDataImport::GetNameFromToken
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
 - IMetaDataImport.GetNameFromToken
---

# IMetaDataImport::GetNameFromToken


## -description

Gets the UTF-8 name of the object referenced by the specified metadata token. This method is obsolete.

## -parameters

### -param tk [in]

The token representing the object to return the name for.

### -param pszUtf8NamePtr [out]

A pointer to the UTF-8 object name in the heap.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>GetNameFromToken</b> is obsolete. As an alternative, call a method to get the properties of the particular type of token required, such as <a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getfieldprops">GetFieldProps</a> for a field or <a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getmethodprops">GetMethodProps</a> for a method.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>