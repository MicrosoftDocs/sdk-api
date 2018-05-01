---
UID: NF:rometadataapi.IMetaDataTables.GetTableInfo
title: IMetaDataTables::GetTableInfo method
author: windows-driver-content
description: Gets the name, row size, number of rows, number of columns, and key column index of the specified table.
old-location: winrt\imetadatatables_gettableinfo.htm
old-project: WinRT
ms.assetid: a2ba07df-4ccf-4563-b540-821008fc985c
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: GetTableInfo method [Windows Runtime], GetTableInfo method [Windows Runtime], IMetaDataTables interface, GetTableInfo,IMetaDataTables.GetTableInfo, IMetaDataTables, IMetaDataTables interface [Windows Runtime], GetTableInfo method, IMetaDataTables::GetTableInfo, rometadataapi/IMetaDataTables::GetTableInfo, winrt.imetadatatables_gettableinfo
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
-	IMetaDataTables.GetTableInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMetaDataTables::GetTableInfo method


## -description


Gets the name, row size, number of rows, number of columns, and key column index of the specified table.


## -parameters




### -param ixTbl [in]

The identifier of the table whose properties to return.


### -param pcbRow [out]

A pointer to the size, in bytes, of a table row.


### -param pcRows [out]

A pointer to the number of rows in the table.


### -param pcCols [out]

 A pointer to the number of columns in the table.


### -param piKey [out]

A pointer to the index of the key column, or -1 if the table has no key column.


### -param ppName [out]

A pointer to a pointer to the table name.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/30d06e87-93a2-4a9c-8843-4c42d7d9e3c8">IMetaDataTables</a>
 

 

