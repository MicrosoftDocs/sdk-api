---
UID: NF:rometadataapi.IMetaDataTables.GetTableInfo
title: IMetaDataTables::GetTableInfo (rometadataapi.h)
description: Gets the name, row size, number of rows, number of columns, and key column index of the specified table.
old-location: winrt\imetadatatables_gettableinfo.htm
tech.root: WinRT
ms.assetid: a2ba07df-4ccf-4563-b540-821008fc985c
ms.date: 12/05/2018
ms.keywords: GetTableInfo, GetTableInfo method [Windows Runtime], GetTableInfo method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetTableInfo method, IMetaDataTables.GetTableInfo, IMetaDataTables::GetTableInfo, rometadataapi/IMetaDataTables::GetTableInfo, winrt.imetadatatables_gettableinfo
ms.topic: method
f1_keywords:
- rometadataapi/IMetaDataTables.GetTableInfo
dev_langs:
- c++
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
- IMetaDataTables.GetTableInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataTables::GetTableInfo


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




<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>
 

 

