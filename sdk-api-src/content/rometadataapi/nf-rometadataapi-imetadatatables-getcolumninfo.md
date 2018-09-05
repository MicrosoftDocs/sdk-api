---
UID: NF:rometadataapi.IMetaDataTables.GetColumnInfo
title: IMetaDataTables::GetColumnInfo
author: windows-sdk-content
description: Gets data about the specified column in the specified table.
old-location: winrt\imetadatatables_getcolumninfo.htm
old-project: WinRT
ms.assetid: aea7944a-87db-496c-869d-e9e2fa87e9af
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetColumnInfo, GetColumnInfo method [Windows Runtime], GetColumnInfo method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetColumnInfo method, IMetaDataTables.GetColumnInfo, IMetaDataTables::GetColumnInfo, rometadataapi/IMetaDataTables::GetColumnInfo, winrt.imetadatatables_getcolumninfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rometadataapi.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataTables.GetColumnInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataTables::GetColumnInfo


## -description


Gets data about the specified column in the specified table.


## -parameters




### -param ixTbl [in]

The index of the desired table.


### -param ixCol [in]

The index of the desired column.


### -param poCol [out]

A pointer to the offset of the column in the row.


### -param pcbCol [out]

 A pointer to the size, in bytes, of the column.


### -param pType [out]

A pointer to the type of the values in the column.


### -param ppName [out]

A pointer to a pointer to the column name.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/30d06e87-93a2-4a9c-8843-4c42d7d9e3c8">IMetaDataTables</a>
 

 

