---
UID: NF:rometadataapi.IMetaDataImport.EnumInterfaceImpls
title: IMetaDataImport::EnumInterfaceImpls (rometadataapi.h)
description: Enumerates MethodDef tokens representing interface implementations.
helpviewer_keywords: ["EnumInterfaceImpls","EnumInterfaceImpls method [Windows Runtime]","EnumInterfaceImpls method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumInterfaceImpls method","IMetaDataImport.EnumInterfaceImpls","IMetaDataImport::EnumInterfaceImpls","rometadataapi/IMetaDataImport::EnumInterfaceImpls","winrt.imetadataimport_enuminterfaceimpls"]
old-location: winrt\imetadataimport_enuminterfaceimpls.htm
tech.root: WinRT
ms.assetid: 37f3eada-7719-4303-a9c7-57ee396a5dc5
ms.date: 12/05/2018
ms.keywords: EnumInterfaceImpls, EnumInterfaceImpls method [Windows Runtime], EnumInterfaceImpls method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumInterfaceImpls method, IMetaDataImport.EnumInterfaceImpls, IMetaDataImport::EnumInterfaceImpls, rometadataapi/IMetaDataImport::EnumInterfaceImpls, winrt.imetadataimport_enuminterfaceimpls
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
 - IMetaDataImport::EnumInterfaceImpls
 - rometadataapi/IMetaDataImport::EnumInterfaceImpls
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
 - IMetaDataImport.EnumInterfaceImpls
---

# IMetaDataImport::EnumInterfaceImpls


## -description

Enumerates InterfaceImpl tokens representing interface implementations.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator.

### -param td [in]

The token of the TypeDef whose InterfaceImpl tokens representing interface implementations are to be enumerated.

### -param rImpls [out]

The array used to store the InterfaceImpl tokens.

### -param cMax [in]

The maximum size of the <i>rImpls</i> array.

### -param pcImpls [out, retval]

The actual number of tokens returned in <i>rImpls</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumInterfaceImpls</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no InterfaceImpl tokens to enumerate. In this case, <i>pcImpls</i> is 0 (zero).
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>
