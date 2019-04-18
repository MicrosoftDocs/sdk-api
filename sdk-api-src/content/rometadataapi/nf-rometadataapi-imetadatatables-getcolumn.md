---
UID: NF:rometadataapi.IMetaDataTables.GetColumn
title: IMetaDataTables::GetColumn (rometadataapi.h)
author: windows-sdk-content
description: Gets a pointer to the value contained in the cell of the specified column and row in the given table.
old-location: winrt\imetadatatables_getcolumn.htm
tech.root: WinRT
ms.assetid: 69f80c79-5587-4740-b996-6c996e40ccf4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetColumn, GetColumn method [Windows Runtime], GetColumn method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetColumn method, IMetaDataTables.GetColumn, IMetaDataTables::GetColumn, rometadataapi/IMetaDataTables::GetColumn, winrt.imetadatatables_getcolumn
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
 - IMetaDataTables.GetColumn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataTables::GetColumn


## -description


Gets a pointer to the value contained in the cell of the specified column and row in the given table.


## -parameters




### -param ixTbl [in]

The index of the table.


### -param ixCol [in]

The index of the column in the table.


### -param rid [in]

The index of the row in the table.


### -param pVal [out]

A pointer to the value in the cell.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/30d06e87-93a2-4a9c-8843-4c42d7d9e3c8">IMetaDataTables</a>
 

 

