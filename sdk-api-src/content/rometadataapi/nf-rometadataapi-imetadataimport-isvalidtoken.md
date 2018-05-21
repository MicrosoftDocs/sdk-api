---
UID: NF:rometadataapi.IMetaDataImport.IsValidToken
title: IMetaDataImport::IsValidToken
author: windows-driver-content
description: Gets a value indicating whether the specified token holds a valid reference to a code object.
old-location: winrt\imetadataimport_isvalidtoken.htm
old-project: WinRT
ms.assetid: 9829a600-38fb-48ac-a486-abb56d17afdf
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: IMetaDataImport interface [Windows Runtime],IsValidToken method, IMetaDataImport.IsValidToken, IMetaDataImport::IsValidToken, IsValidToken, IsValidToken method [Windows Runtime], IsValidToken method [Windows Runtime],IMetaDataImport interface, rometadataapi/IMetaDataImport::IsValidToken, winrt.imetadataimport_isvalidtoken
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
-	IMetaDataImport.IsValidToken
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMetaDataImport::IsValidToken


## -description


Gets a value indicating whether the specified token holds a valid reference to a code object.


## -parameters




### -param tk [in]

The token to check the reference validity for.


## -returns



<b>true</b> if <i>tk</i> is a valid metadata token within the current scope. Otherwise, <b>false</b>.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

