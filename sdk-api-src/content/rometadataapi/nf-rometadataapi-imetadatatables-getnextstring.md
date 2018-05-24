---
UID: NF:rometadataapi.IMetaDataTables.GetNextString
title: IMetaDataTables::GetNextString
author: windows-driver-content
description: Gets the index of the next string in the current table column.
old-location: winrt\imetadatatables_getnextstring.htm
old-project: WinRT
ms.assetid: 7ac1fc2c-a60d-4431-8e49-5df1bb078c9b
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: GetNextString, GetNextString method [Windows Runtime], GetNextString method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetNextString method, IMetaDataTables.GetNextString, IMetaDataTables::GetNextString, rometadataapi/IMetaDataTables::GetNextString, winrt.imetadatatables_getnextstring
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
-	IMetaDataTables.GetNextString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMetaDataTables::GetNextString


## -description


Gets the index of the next string in the current table column.


## -parameters




### -param ixString [in]

The index value from a string table column.


### -param pNext [out]

A pointer to the index of the next string in the column.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/30d06e87-93a2-4a9c-8843-4c42d7d9e3c8">IMetaDataTables</a>
 

 

