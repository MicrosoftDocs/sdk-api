---
UID: NF:rometadataapi.IMetaDataImport.EnumUnresolvedMethods
title: IMetaDataImport::EnumUnresolvedMethods (rometadataapi.h)
description: Enumerates MemberDef tokens representing the unresolved methods in the current metadata scope.
helpviewer_keywords: ["EnumUnresolvedMethods","EnumUnresolvedMethods method [Windows Runtime]","EnumUnresolvedMethods method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumUnresolvedMethods method","IMetaDataImport.EnumUnresolvedMethods","IMetaDataImport::EnumUnresolvedMethods","rometadataapi/IMetaDataImport::EnumUnresolvedMethods","winrt.imetadataimport_enumunresolvedmethods"]
old-location: winrt\imetadataimport_enumunresolvedmethods.htm
tech.root: WinRT
ms.assetid: 8c10a1af-93a5-44d0-818f-f307f5f81075
ms.date: 12/05/2018
ms.keywords: EnumUnresolvedMethods, EnumUnresolvedMethods method [Windows Runtime], EnumUnresolvedMethods method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumUnresolvedMethods method, IMetaDataImport.EnumUnresolvedMethods, IMetaDataImport::EnumUnresolvedMethods, rometadataapi/IMetaDataImport::EnumUnresolvedMethods, winrt.imetadataimport_enumunresolvedmethods
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
 - IMetaDataImport::EnumUnresolvedMethods
 - rometadataapi/IMetaDataImport::EnumUnresolvedMethods
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
 - IMetaDataImport.EnumUnresolvedMethods
---

# IMetaDataImport::EnumUnresolvedMethods


## -description

Enumerates MemberDef tokens representing the unresolved methods in the current metadata scope.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator. This must be NULL for the first call of this method.

### -param rgMethods [out]

The array used to store the MemberDef tokens.

### -param cMax [in]

The maximum size of the <i>rgMethods</i> array.

### -param pcTokens [out]

The number of MemberDef tokens returned in <i>rgMethods</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumUnresolvedMethods</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>

## -remarks

An unresolved method is one that has been declared but not implemented. A method is included in the enumeration if the method is marked <b>miForwardRef</b> and either <b>mdPinvokeImpl</b> or <b>miRuntime</b> is set to zero. In other words, an unresolved method is a class method that is marked <b>miForwardRef</b> but which is not implemented in unmanaged code (reached via PInvoke) nor implemented internally by the runtime itself. 



The enumeration excludes all methods that are defined either at module scope (globals) or in interfaces or abstract classes.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>