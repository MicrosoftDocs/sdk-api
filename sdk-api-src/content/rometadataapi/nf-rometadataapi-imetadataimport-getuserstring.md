---
UID: NF:rometadataapi.IMetaDataImport.GetUserString
title: IMetaDataImport::GetUserString
author: windows-sdk-content
description: Gets the literal string represented by the specified metadata token.
old-location: winrt\imetadataimport_getuserstring.htm
tech.root: WinRT
ms.assetid: c809d878-7c9a-4759-83c8-31cb0a72ee9d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetUserString, GetUserString method [Windows Runtime], GetUserString method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetUserString method, IMetaDataImport.GetUserString, IMetaDataImport::GetUserString, rometadataapi/IMetaDataImport::GetUserString, winrt.imetadataimport_getuserstring
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
 - IMetaDataImport.GetUserString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataImport::GetUserString


## -description


Gets the literal string represented by the specified metadata token.


## -parameters




### -param tkString [in]

The String token to return the associated string for.


### -param szString [out]

A copy of the requested string.


### -param cchString [in]

The maximum size in wide characters of the requested <i>szString</i>.


### -param pchString [out]

The size in wide characters of the returned <i>szString</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

