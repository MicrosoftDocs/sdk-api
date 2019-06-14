---
UID: NF:rometadataapi.IMetaDataTables.GetNextString
title: IMetaDataTables::GetNextString (rometadataapi.h)
author: windows-sdk-content
description: Gets the index of the next string in the current table column.
old-location: winrt\imetadatatables_getnextstring.htm
tech.root: WinRT
ms.assetid: 7ac1fc2c-a60d-4431-8e49-5df1bb078c9b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetNextString, GetNextString method [Windows Runtime], GetNextString method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetNextString method, IMetaDataTables.GetNextString, IMetaDataTables::GetNextString, rometadataapi/IMetaDataTables::GetNextString, winrt.imetadatatables_getnextstring
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
 - IMetaDataTables.GetNextString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>
 

 

