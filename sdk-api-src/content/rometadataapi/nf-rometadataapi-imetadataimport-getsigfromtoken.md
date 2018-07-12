---
UID: NF:rometadataapi.IMetaDataImport.GetSigFromToken
title: IMetaDataImport::GetSigFromToken
author: windows-sdk-content
description: Gets the binary metadata signature associated with the specified token.
old-location: winrt\imetadataimport_getsigfromtoken.htm
old-project: WinRT
ms.assetid: babd95ef-7786-47da-b5f6-c1fef93a4504
ms.author: windowssdkdev
ms.date: 07/06/2018
ms.keywords: GetSigFromToken, GetSigFromToken method [Windows Runtime], GetSigFromToken method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetSigFromToken method, IMetaDataImport.GetSigFromToken, IMetaDataImport::GetSigFromToken, rometadataapi/IMetaDataImport::GetSigFromToken, winrt.imetadataimport_getsigfromtoken
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
 - IMetaDataImport.GetSigFromToken
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataImport::GetSigFromToken


## -description


Gets the binary metadata signature associated with the specified token.


## -parameters




### -param tkSignature [in]

The token to return the binary metadata signature for.


### -param ppvSig [out]

A pointer to the returned metadata signature.


### -param pcbSig [out]

The size in bytes of the binary metadata signature.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

