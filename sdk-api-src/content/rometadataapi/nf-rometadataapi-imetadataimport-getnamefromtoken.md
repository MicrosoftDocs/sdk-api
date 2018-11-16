---
UID: NF:rometadataapi.IMetaDataImport.GetNameFromToken
title: IMetaDataImport::GetNameFromToken
author: windows-sdk-content
description: Gets the UTF-8 name of the object referenced by the specified metadata token. This method is obsolete.
old-location: winrt\imetadataimport_getnamefromtoken.htm
tech.root: WinRT
ms.assetid: 933d502a-c752-45ae-b51f-8c0a876856bc
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetNameFromToken, GetNameFromToken method [Windows Runtime], GetNameFromToken method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetNameFromToken method, IMetaDataImport.GetNameFromToken, IMetaDataImport::GetNameFromToken, rometadataapi/IMetaDataImport::GetNameFromToken, winrt.imetadataimport_getnamefromtoken
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
 - IMetaDataImport.GetNameFromToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- rometadataapi.h
: 
- IMetaDataImport.GetNameFromToken
: 
---

# IMetaDataImport::GetNameFromToken


## -description


Gets the UTF-8 name of the object referenced by the specified metadata token. This method is obsolete.


## -parameters




### -param tk [in]

The token representing the object to return the name for.


### -param pszUtf8NamePtr [out]

A pointer to the UTF-8 object name in the heap.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>GetNameFromToken</b> is obsolete. As an alternative, call a method to get the properties of the particular type of token required, such as <a href="https://msdn.microsoft.com/6c935c4c-a7ac-49b9-af26-25f240ef78f2">GetFieldProps</a> for a field or <a href="https://msdn.microsoft.com/973f2a8c-025d-4d27-ac99-56902b1132dd">GetMethodProps</a> for a method.






## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

