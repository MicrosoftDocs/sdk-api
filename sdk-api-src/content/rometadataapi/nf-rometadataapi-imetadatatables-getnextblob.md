---
UID: NF:rometadataapi.IMetaDataTables.GetNextBlob
title: IMetaDataTables::GetNextBlob
author: windows-sdk-content
description: Gets the index of the next binary large object (BLOB) in the table.
old-location: winrt\imetadatatables_getnextblob.htm
old-project: WinRT
ms.assetid: f70e5377-4cc1-4066-acc2-bb13f336881b
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: GetNextBlob, GetNextBlob method [Windows Runtime], GetNextBlob method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetNextBlob method, IMetaDataTables.GetNextBlob, IMetaDataTables::GetNextBlob, rometadataapi/IMetaDataTables::GetNextBlob, winrt.imetadatatables_getnextblob
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataTables.GetNextBlob
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMetaDataTables::GetNextBlob


## -description


Gets the index of the next binary large object (BLOB) in the table.


## -parameters




### -param ixBlob [in]

The index, as returned from a column of BLOBs.


### -param pNext [out]

A pointer to the index of the next BLOB.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/30d06e87-93a2-4a9c-8843-4c42d7d9e3c8">IMetaDataTables</a>
 

 

