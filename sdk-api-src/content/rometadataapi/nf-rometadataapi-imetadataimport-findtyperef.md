---
UID: NF:rometadataapi.IMetaDataImport.FindTypeRef
title: IMetaDataImport::FindTypeRef
author: windows-sdk-content
description: Gets a pointer to the TypeRef token for the Type reference that is in the specified scope and that has the specified name.
old-location: winrt\imetadataimport_findtyperef.htm
tech.root: WinRT
ms.assetid: ec89d7c0-b607-4885-b819-3eb8022ad46d
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: FindTypeRef, FindTypeRef method [Windows Runtime], FindTypeRef method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],FindTypeRef method, IMetaDataImport.FindTypeRef, IMetaDataImport::FindTypeRef, rometadataapi/IMetaDataImport::FindTypeRef, winrt.imetadataimport_findtyperef
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




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

