---
UID: NF:rometadataapi.IMetaDataImport.EnumEvents
title: IMetaDataImport::EnumEvents (rometadataapi.h)
description: Enumerates event definition tokens for the specified TypeDef token.
helpviewer_keywords: ["EnumEvents","EnumEvents method [Windows Runtime]","EnumEvents method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumEvents method","IMetaDataImport.EnumEvents","IMetaDataImport::EnumEvents","rometadataapi/IMetaDataImport::EnumEvents","winrt.imetadataimport_enumevents"]
old-location: winrt\imetadataimport_enumevents.htm
tech.root: WinRT
ms.assetid: 442b5db1-1e5f-4314-9c53-dbd0f0651d3c
ms.date: 12/05/2018
ms.keywords: EnumEvents, EnumEvents method [Windows Runtime], EnumEvents method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumEvents method, IMetaDataImport.EnumEvents, IMetaDataImport::EnumEvents, rometadataapi/IMetaDataImport::EnumEvents, winrt.imetadataimport_enumevents
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
 - IMetaDataImport::EnumEvents
 - rometadataapi/IMetaDataImport::EnumEvents
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
 - IMetaDataImport.EnumEvents
---

# IMetaDataImport::EnumEvents


## -description

Enumerates event definition tokens for the specified TypeDef token.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator.

### -param tkTypDef [in]

The TypeDef token whose event definitions are to be enumerated.

### -param rgEvents [out]

The array of returned events.

### -param cMax [in]

The maximum size of the <i>rgEvents</i> array.

### -param pcEvents [out]

The actual number of events returned in <i>rgEvents</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumEvents</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no events to enumerate. In this case, <i>pcEvents</i> is zero.
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>