---
UID: NF:rometadataapi.IMetaDataImport.EnumUserStrings
title: IMetaDataImport::EnumUserStrings (rometadataapi.h)
description: Enumerates String tokens representing hard-coded strings in the current metadata scope.
helpviewer_keywords: ["EnumUserStrings","EnumUserStrings method [Windows Runtime]","EnumUserStrings method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumUserStrings method","IMetaDataImport.EnumUserStrings","IMetaDataImport::EnumUserStrings","rometadataapi/IMetaDataImport::EnumUserStrings","winrt.imetadataimport_enumuserstrings"]
old-location: winrt\imetadataimport_enumuserstrings.htm
tech.root: WinRT
ms.assetid: 646f6e8a-4c78-493c-90e2-2114bce82c46
ms.date: 12/05/2018
ms.keywords: EnumUserStrings, EnumUserStrings method [Windows Runtime], EnumUserStrings method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumUserStrings method, IMetaDataImport.EnumUserStrings, IMetaDataImport::EnumUserStrings, rometadataapi/IMetaDataImport::EnumUserStrings, winrt.imetadataimport_enumuserstrings
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
 - IMetaDataImport::EnumUserStrings
 - rometadataapi/IMetaDataImport::EnumUserStrings
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
 - IMetaDataImport.EnumUserStrings
---

# IMetaDataImport::EnumUserStrings


## -description

Enumerates String tokens representing hard-coded strings in the current metadata scope.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator. This must be NULL for the first call of this method.

### -param rgStrings [out]

The array used to store the String tokens.

### -param cMax [in]

The maximum size of the <i>rgStrings</i> array.

### -param pcStrings [out]

The number of String tokens returned in <i>rgStrings</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumUserStrings</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcStrings</i> is 0 (zero).
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>