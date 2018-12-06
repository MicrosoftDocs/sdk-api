---
UID: NF:rometadataapi.IMetaDataTables.GetBlob
title: IMetaDataTables::GetBlob
author: windows-sdk-content
description: Gets a pointer to the binary large object (BLOB) at the specified column index.
old-location: winrt\imetadatatables_getblob.htm
tech.root: WinRT
ms.assetid: 1a9da245-a1a9-4004-8925-00b2fe72c9ca
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetBlob, GetBlob method [Windows Runtime], GetBlob method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetBlob method, IMetaDataTables.GetBlob, IMetaDataTables::GetBlob, rometadataapi/IMetaDataTables::GetBlob, winrt.imetadatatables_getblob
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
 - IMetaDataTables.GetBlob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataTables::GetBlob


## -description


Gets a pointer to the binary large object (BLOB) at the specified column index.


## -parameters




### -param ixBlob [in]

The memory address from which to get <i>ppData</i>.


### -param pcbData [out]

A pointer to the size, in bytes, of <i>ppData</i>.


### -param ppData [out]

A pointer to a pointer to the binary data retrieved.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/30d06e87-93a2-4a9c-8843-4c42d7d9e3c8">IMetaDataTables</a>
 

 

