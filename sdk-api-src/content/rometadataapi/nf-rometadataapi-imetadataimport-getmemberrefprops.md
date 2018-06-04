---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMetaDataImport::GetMemberRefProps


## -description


Gets metadata associated with the member referenced by the specified token.


## -parameters




### -param tkMemberRef [in]

The MemberRef token to return associated metadata for.


### -param ptk [out]

A TypeDef or TypeRef, or TypeSpec token that represents the class that declares the member, or a ModuleRef token that represents the module class that declares the member, or a MethodDef that represents the member.


### -param szMember [out]

A string buffer for the member's name.


### -param cchMember [in]

The requested size in wide characters of <i>szMember</i>.


### -param pchMember [out]

The returned size in wide characters of <i>szMember</i>.


### -param ppvSigBlob [out]

A pointer to the binary metadata signature for the member.


### -param pcbSigBlob [out]

The size in bytes of <i>ppvSigBlob</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

