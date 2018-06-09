---
UID: NF:rometadataapi.IMetaDataImport.GetTypeSpecFromToken
title: IMetaDataImport::GetTypeSpecFromToken
author: windows-sdk-content
description: Gets the binary metadata signature of the type specification represented by the specified token.
old-location: winrt\imetadataimport_gettypespecfromtoken.htm
old-project: WinRT
ms.assetid: e03b6c5f-c68a-44a9-a203-8ed00293b582
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetTypeSpecFromToken, GetTypeSpecFromToken method [Windows Runtime], GetTypeSpecFromToken method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetTypeSpecFromToken method, IMetaDataImport.GetTypeSpecFromToken, IMetaDataImport::GetTypeSpecFromToken, rometadataapi/IMetaDataImport::GetTypeSpecFromToken, winrt.imetadataimport_gettypespecfromtoken
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataImport.GetTypeSpecFromToken
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMetaDataImport::GetTypeSpecFromToken


## -description


Gets the binary metadata signature of the type specification represented by the specified token.


## -parameters




### -param tkTypeSpec [in]

The TypeSpec token associated with the requested metadata signature.


### -param ppvSig [out]

 A pointer to the binary metadata signature.


### -param pcbSig [out]

The size, in bytes, of the metadata signature.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

