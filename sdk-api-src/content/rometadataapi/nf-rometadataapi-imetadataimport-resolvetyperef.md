---
UID: NF:rometadataapi.IMetaDataImport.ResolveTypeRef
title: IMetaDataImport::ResolveTypeRef (rometadataapi.h)
description: Resolves a Type reference represented by the specified TypeRef token.
helpviewer_keywords: ["IMetaDataImport interface [Windows Runtime]","ResolveTypeRef method","IMetaDataImport.ResolveTypeRef","IMetaDataImport::ResolveTypeRef","ResolveTypeRef","ResolveTypeRef method [Windows Runtime]","ResolveTypeRef method [Windows Runtime]","IMetaDataImport interface","rometadataapi/IMetaDataImport::ResolveTypeRef","winrt.imetadataimport_resolvetyperef"]
old-location: winrt\imetadataimport_resolvetyperef.htm
tech.root: WinRT
ms.assetid: d19d47c7-bf06-4daa-bda6-8aca6939a543
ms.date: 12/05/2018
ms.keywords: IMetaDataImport interface [Windows Runtime],ResolveTypeRef method, IMetaDataImport.ResolveTypeRef, IMetaDataImport::ResolveTypeRef, ResolveTypeRef, ResolveTypeRef method [Windows Runtime], ResolveTypeRef method [Windows Runtime],IMetaDataImport interface, rometadataapi/IMetaDataImport::ResolveTypeRef, winrt.imetadataimport_resolvetyperef
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
 - IMetaDataImport::ResolveTypeRef
 - rometadataapi/IMetaDataImport::ResolveTypeRef
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
 - IMetaDataImport.ResolveTypeRef
---

# IMetaDataImport::ResolveTypeRef


## -description

Resolves a Type reference represented by the specified TypeRef token.

## -parameters

### -param tkTypeRef [in]

The TypeRef metadata token to return the referenced type information for.

### -param riid [in]

The IID of the interface to return in ppIScope. Typically, this would be IID_IMetaDataImport.

### -param ppIScope [out]

An interface to the module scope in which the referenced type is defined.

### -param ptkTypeDef [out, retval]

A pointer to a TypeDef token that represents the referenced type.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Important</b>  Do not use this method if multiple application domains are loaded. The method does not respect application domain boundaries. If multiple versions of an assembly are loaded, and they contain the same type with the same namespace, the method returns the module scope of the first type it finds.
 

</div>
<div> </div>
The <b>ResolveTypeRef</b> method searches for the type definition in other modules. If the type definition is found, <b>ResolveTypeRef</b> returns an interface to that module scope as well as the TypeDef token for the type.

If the type reference to be resolved has a resolution scope of AssemblyRef, the <b>ResolveTypeRef</b> method searches for a match only in the metadata scopes that have already been opened with calls to either the <a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatadispenser-openscope">IMetaDataDispenser::OpenScope</a> method or the <a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatadispenser-openscopeonmemory">IMetaDataDispenser::OpenScopeOnMemory</a> method. This is because <b>ResolveTypeRef</b> cannot determine from only the AssemblyRef scope where on disk or in the global assembly cache the assembly is stored.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>