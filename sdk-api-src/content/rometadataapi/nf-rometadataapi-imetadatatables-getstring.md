---
UID: NF:rometadataapi.IMetaDataTables.GetString
title: IMetaDataTables::GetString
author: windows-sdk-content
description: Gets the string at the specified index from the table column in the current reference scope.
old-location: winrt\imetadatatables_getstring.htm
old-project: WinRT
ms.assetid: 35b79dac-39c7-4ca2-8608-e7ea64d4574c
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: GetString, GetString method [Windows Runtime], GetString method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetString method, IMetaDataTables.GetString, IMetaDataTables::GetString, rometadataapi/IMetaDataTables::GetString, winrt.imetadatatables_getstring
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	rometadataapi.h
api_name:
-	IMetaDataTables.GetString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMetaDataTables::GetString


## -description


Gets the string at the specified index from the table column in the current reference scope.


## -parameters




### -param ixString [in]

The index at which to start to search for the next value.


### -param ppString [out]

A pointer to a pointer to the returned string value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/30d06e87-93a2-4a9c-8843-4c42d7d9e3c8">IMetaDataTables</a>
 

 

