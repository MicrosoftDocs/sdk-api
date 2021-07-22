---
UID: NF:mfidl.IMFMetadata.GetAllPropertyNames
title: IMFMetadata::GetAllPropertyNames (mfidl.h)
description: Gets a list of all the metadata property names on this object.
helpviewer_keywords: ["GetAllPropertyNames","GetAllPropertyNames method [Media Foundation]","GetAllPropertyNames method [Media Foundation]","IMFMetadata interface","IMFMetadata interface [Media Foundation]","GetAllPropertyNames method","IMFMetadata.GetAllPropertyNames","IMFMetadata::GetAllPropertyNames","e0944d42-d6e6-420d-9980-ca6c62736b3d","mf.imfmetadata_getallpropertynames","mfidl/IMFMetadata::GetAllPropertyNames"]
old-location: mf\imfmetadata_getallpropertynames.htm
tech.root: mf
ms.assetid: e0944d42-d6e6-420d-9980-ca6c62736b3d
ms.date: 12/05/2018
ms.keywords: GetAllPropertyNames, GetAllPropertyNames method [Media Foundation], GetAllPropertyNames method [Media Foundation],IMFMetadata interface, IMFMetadata interface [Media Foundation],GetAllPropertyNames method, IMFMetadata.GetAllPropertyNames, IMFMetadata::GetAllPropertyNames, e0944d42-d6e6-420d-9980-ca6c62736b3d, mf.imfmetadata_getallpropertynames, mfidl/IMFMetadata::GetAllPropertyNames
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMetadata::GetAllPropertyNames
 - mfidl/IMFMetadata::GetAllPropertyNames
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMetadata.GetAllPropertyNames
---

# IMFMetadata::GetAllPropertyNames


## -description

Gets a list of all the metadata property names on this object.

## -parameters

### -param ppvNames [out]

Pointer to a <b>PROPVARIANT</b> that receives an array of null-terminated wide-character strings. If no properties are available, the <b>PROPVARIANT</b> type is VT_EMPTY. Otherwise, the <b>PROPVARIANT</b> type is VT_VECTOR | VT_LPWSTR. The caller must free the <b>PROPVARIANT</b> by calling <a href="/windows/desktop/api/propidl/nf-propidl-propvariantclear">PropVariantClear</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadata">IMFMetadata</a>



<a href="/windows/desktop/medfound/media-metadata">Media Metadata</a>