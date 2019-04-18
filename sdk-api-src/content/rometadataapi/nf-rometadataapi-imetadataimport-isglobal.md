---
UID: NF:rometadataapi.IMetaDataImport.IsGlobal
title: IMetaDataImport::IsGlobal (rometadataapi.h)
author: windows-sdk-content
description: Gets a value indicating whether the field, method, or type represented by the specified metadata token has global scope.
old-location: winrt\imetadataimport_isglobal.htm
tech.root: WinRT
ms.assetid: 01558f0f-11ca-4c17-8f55-b0fc78492813
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMetaDataImport interface [Windows Runtime],IsGlobal method, IMetaDataImport.IsGlobal, IMetaDataImport::IsGlobal, IsGlobal, IsGlobal method [Windows Runtime], IsGlobal method [Windows Runtime],IMetaDataImport interface, rometadataapi/IMetaDataImport::IsGlobal, winrt.imetadataimport_isglobal
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
 - IMetaDataImport.IsGlobal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataImport::IsGlobal


## -description


Gets a value indicating whether the field, method, or type represented by the specified metadata token has global scope.


## -parameters




### -param tk [in]

A metadata token that represents a type, field, or method.


### -param pbIsGlobal [out]

1 if the object has global scope; otherwise, 0 (zero).


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

