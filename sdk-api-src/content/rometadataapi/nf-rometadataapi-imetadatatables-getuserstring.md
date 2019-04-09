---
UID: NF:rometadataapi.IMetaDataTables.GetUserString
title: IMetaDataTables::GetUserString (rometadataapi.h)
author: windows-sdk-content
description: Gets the hard-coded string at the specified index in the string column in the current scope.
old-location: winrt\imetadatatables_getuserstring.htm
tech.root: WinRT
ms.assetid: 868f6be3-1baf-4f7c-be10-12b79a45e9c7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetUserString, GetUserString method [Windows Runtime], GetUserString method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetUserString method, IMetaDataTables.GetUserString, IMetaDataTables::GetUserString, rometadataapi/IMetaDataTables::GetUserString, winrt.imetadatatables_getuserstring
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
 - IMetaDataTables.GetUserString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataTables::GetUserString


## -description


Gets the hard-coded string at the specified index in the string column in the current scope.


## -parameters




### -param ixUserString [in]

The index value from which the hard-coded string will be retrieved.


### -param pcbData [out]

A pointer to the size of <i>ppData</i>.


### -param ppData [out]

A pointer to a pointer to the returned string.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/30d06e87-93a2-4a9c-8843-4c42d7d9e3c8">IMetaDataTables</a>
 

 

