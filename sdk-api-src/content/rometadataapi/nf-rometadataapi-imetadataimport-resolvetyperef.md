---
UID: NF:rometadataapi.IMetaDataImport.ResolveTypeRef
title: IMetaDataImport::ResolveTypeRef
author: windows-driver-content
description: Resolves a Type reference represented by the specified TypeRef token.
old-location: winrt\imetadataimport_resolvetyperef.htm
old-project: WinRT
ms.assetid: d19d47c7-bf06-4daa-bda6-8aca6939a543
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: IMetaDataImport interface [Windows Runtime],ResolveTypeRef method, IMetaDataImport.ResolveTypeRef, IMetaDataImport::ResolveTypeRef, ResolveTypeRef, ResolveTypeRef method [Windows Runtime], ResolveTypeRef method [Windows Runtime],IMetaDataImport interface, rometadataapi/IMetaDataImport::ResolveTypeRef, winrt.imetadataimport_resolvetyperef
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	rometadataapi.h
api_name:
-	IMetaDataImport.ResolveTypeRef
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Important</b>  Do not use this method if multiple application domains are loaded. The method does not respect application domain boundaries. If multiple versions of an assembly are loaded, and they contain the same type with the same namespace, the method returns the module scope of the first type it finds.
 

</div>
<div> </div>
The <b>ResolveTypeRef</b> method searches for the type definition in other modules. If the type definition is found, <b>ResolveTypeRef</b> returns an interface to that module scope as well as the TypeDef token for the type.

If the type reference to be resolved has a resolution scope of AssemblyRef, the <b>ResolveTypeRef</b> method searches for a match only in the metadata scopes that have already been opened with calls to either the <a href="https://msdn.microsoft.com/77ba5ee6-082c-478f-83fc-7f6c31ee3c74">IMetaDataDispenser::OpenScope</a> method or the <a href="https://msdn.microsoft.com/4558b229-0fe9-4ff7-a666-e69b47cb8170">IMetaDataDispenser::OpenScopeOnMemory</a> method. This is because <b>ResolveTypeRef</b> cannot determine from only the AssemblyRef scope where on disk or in the global assembly cache the assembly is stored.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

