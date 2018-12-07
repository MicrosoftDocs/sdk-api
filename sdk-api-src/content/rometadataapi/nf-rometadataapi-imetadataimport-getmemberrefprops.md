---
UID: NF:rometadataapi.IMetaDataImport.GetMemberRefProps
title: IMetaDataImport::GetMemberRefProps
author: windows-sdk-content
description: Gets metadata associated with the member referenced by the specified token.
old-location: winrt\imetadataimport_getmemberrefprops.htm
tech.root: WinRT
ms.assetid: a82baa9a-0102-4d30-945d-34ec2514e0a6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMemberRefProps, GetMemberRefProps method [Windows Runtime], GetMemberRefProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetMemberRefProps method, IMetaDataImport.GetMemberRefProps, IMetaDataImport::GetMemberRefProps, rometadataapi/IMetaDataImport::GetMemberRefProps, winrt.imetadataimport_getmemberrefprops
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
 - IMetaDataImport.GetMemberRefProps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

