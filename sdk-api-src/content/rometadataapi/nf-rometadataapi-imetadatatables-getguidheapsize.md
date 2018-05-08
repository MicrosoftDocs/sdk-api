---
UID: NF:rometadataapi.IMetaDataTables.GetGuidHeapSize
title: IMetaDataTables::GetGuidHeapSize
author: windows-driver-content
description: Gets the size, in bytes, of the GUID heap.
old-location: winrt\imetadatatables_getguidheapsize.htm
old-project: WinRT
ms.assetid: 56b0f15f-caf3-44e0-8cec-7ca3f2edb74d
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: GetGuidHeapSize, GetGuidHeapSize method [Windows Runtime], GetGuidHeapSize method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetGuidHeapSize method, IMetaDataTables.GetGuidHeapSize, IMetaDataTables::GetGuidHeapSize, rometadataapi/IMetaDataTables::GetGuidHeapSize, winrt.imetadatatables_getguidheapsize
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
-	IMetaDataTables.GetGuidHeapSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMetaDataTables::GetGuidHeapSize


## -description


Gets the size, in bytes, of the GUID heap.


## -parameters




### -param pcbGuids [out]

A pointer to the size, in bytes, of the GUID heap.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/30d06e87-93a2-4a9c-8843-4c42d7d9e3c8">IMetaDataTables</a>
 

 

