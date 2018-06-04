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

# IMetaDataImport::GetMemberProps


## -description


Gets metadata information, including the name, binary signature, and relative virtual address, of the Type member referenced by the specified metadata token.


## -parameters




### -param tkMember [in]

The token that references the member to get the associated metadata for.


### -param ptkTypeDef [out]

A pointer to the metadata token that represents the class of the member.


### -param szMember [out]

The name of the member.


### -param cchMember [in]

The size in wide characters of the szMember buffer.


### -param pchMember [out]

The size in wide characters of the returned name.


### -param pdwAttr [out]

Any flag values applied to the member.


### -param ppvSigBlob [out]

A pointer to the binary metadata signature of the member.


### -param pcbSigBlob [out]

The size in bytes of <i>ppvSigBlob</i>.


### -param pulCodeRVA [out]

A pointer to the relative virtual address of the member.


### -param pdwImplFlags [out]

Any method implementation flags associated with the member.


### -param pdwCPlusTypeFlag [out]

A flag that marks a ValueType.


### -param ppValue [out]

A constant string value returned by this member.


### -param pcchValue [out]

The size in characters of <i>ppValue</i>, or zero if <i>ppValue</i> does not hold a string.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

