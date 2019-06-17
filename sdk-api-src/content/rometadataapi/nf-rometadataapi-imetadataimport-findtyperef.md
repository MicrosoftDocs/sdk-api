---
UID: NF:rometadataapi.IMetaDataImport.FindTypeRef
title: IMetaDataImport::FindTypeRef (rometadataapi.h)
author: windows-sdk-content
description: Gets a pointer to the TypeRef token for the Type reference that is in the specified scope and that has the specified name.
old-location: winrt\imetadataimport_findtyperef.htm
tech.root: WinRT
ms.assetid: ec89d7c0-b607-4885-b819-3eb8022ad46d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FindTypeRef, FindTypeRef method [Windows Runtime], FindTypeRef method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],FindTypeRef method, IMetaDataImport.FindTypeRef, IMetaDataImport::FindTypeRef, rometadataapi/IMetaDataImport::FindTypeRef, winrt.imetadataimport_findtyperef
ms.topic: method
f1_keywords: ["rometadataapi/IMetaDataImport.FindTypeRef"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataImport.FindTypeRef
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataImport::FindTypeRef


## -description


Gets a pointer to the TypeRef token for the Type reference that is in the specified scope and that has the specified name.


## -parameters




### -param tkResolutionScope [in]

A ModuleRef, AssemblyRef, or TypeRef token that specifies the module, assembly, or type, respectively, in which the type reference is defined.


### -param szName [in]

The name of the type reference to search for.


### -param tkTypeRef [out]

A pointer to the matching TypeRef token.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>
 

 

