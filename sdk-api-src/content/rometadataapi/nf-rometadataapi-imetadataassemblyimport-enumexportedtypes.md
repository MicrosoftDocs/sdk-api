---
UID: NF:rometadataapi.IMetaDataAssemblyImport.EnumExportedTypes
title: IMetaDataAssemblyImport::EnumExportedTypes (rometadataapi.h)
description: Enumerates the exported types referenced in the assembly manifest in the current metadata scope.
helpviewer_keywords: ["EnumExportedTypes","EnumExportedTypes method [Windows Runtime]","EnumExportedTypes method [Windows Runtime]","IMetaDataAssemblyImport interface","IMetaDataAssemblyImport interface [Windows Runtime]","EnumExportedTypes method","IMetaDataAssemblyImport.EnumExportedTypes","IMetaDataAssemblyImport::EnumExportedTypes","rometadataapi/IMetaDataAssemblyImport::EnumExportedTypes","winrt.imetadataassemblyimport_enumexportedtypes"]
old-location: winrt\imetadataassemblyimport_enumexportedtypes.htm
tech.root: WinRT
ms.assetid: 8274d8e3-bcfb-4560-b925-2fede03be4cd
ms.date: 12/05/2018
ms.keywords: EnumExportedTypes, EnumExportedTypes method [Windows Runtime], EnumExportedTypes method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],EnumExportedTypes method, IMetaDataAssemblyImport.EnumExportedTypes, IMetaDataAssemblyImport::EnumExportedTypes, rometadataapi/IMetaDataAssemblyImport::EnumExportedTypes, winrt.imetadataassemblyimport_enumexportedtypes
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
 - IMetaDataAssemblyImport::EnumExportedTypes
 - rometadataapi/IMetaDataAssemblyImport::EnumExportedTypes
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
 - IMetaDataAssemblyImport.EnumExportedTypes
---

# IMetaDataAssemblyImport::EnumExportedTypes


## -description

Enumerates the exported types referenced in the assembly manifest in the current metadata scope.

## -parameters

### -param phEnum [in, out]

 A pointer to the enumerator. This must be a null value when the <b>EnumExportedTypes</b> method is called for the first time.

### -param rExportedTypes [out]

The enumeration of <b>mdExportedType</b> metadata tokens.

### -param cMax [in]

The maximum number of <b>mdExportedType</b> tokens that can be placed in the <i>rExportedTypes</i> array.

### -param pcTokens [out]

The number of <b>mdExportedType</b> tokens actually placed in <i>rExportedTypes</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumExportedTypes</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTokens</i> is set to zero.
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport">IMetaDataAssemblyImport</a>