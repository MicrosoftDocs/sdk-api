---
UID: NF:rometadataapi.IMetaDataTables2.GetMetaDataStreamInfo
title: IMetaDataTables2::GetMetaDataStreamInfo
author: windows-sdk-content
description: Gets the name, size, and contents of the metadata stream at the specified index.
old-location: winrt\imetadatatables2_getmetadatastreaminfo.htm
tech.root: WinRT
ms.assetid: a292a32a-b9c2-46b5-a2c4-074e616d7675
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMetaDataStreamInfo, GetMetaDataStreamInfo method [Windows Runtime], GetMetaDataStreamInfo method [Windows Runtime],IMetaDataTables2 interface, IMetaDataTables2 interface [Windows Runtime],GetMetaDataStreamInfo method, IMetaDataTables2.GetMetaDataStreamInfo, IMetaDataTables2::GetMetaDataStreamInfo, rometadataapi/IMetaDataTables2::GetMetaDataStreamInfo, winrt.imetadatatables2_getmetadatastreaminfo
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
 - IMetaDataTables2.GetMetaDataStreamInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataTables2::GetMetaDataStreamInfo


## -description


Gets the name, size, and contents of the metadata stream at the specified index.


## -parameters




### -param ix [in]

The index of the requested metadata stream.


### -param ppchName [out]

A pointer to the name of the stream.


### -param ppv [out]

 A pointer to the metadata stream.


### -param pcb [out]

The size, in bytes, of <i>ppv</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dc59fe85-b490-4f23-a32f-2942610dd8dc">IMetaDataTables2</a>
 

 

