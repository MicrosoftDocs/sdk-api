---
UID: NF:msrdc.ISimilarityTraitsMappedView.Get
title: ISimilarityTraitsMappedView::Get
author: windows-sdk-content
description: Returns information about the mapped view of a similarity traits table file.
old-location: rdc\isimilaritytraitsmappedview_get.htm
old-project: Rdc
ms.assetid: 57542583-528e-49cb-9ece-f49ecfc6b1cd
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: Get, Get method [Remote Differential Compression], Get method [Remote Differential Compression],ISimilarityTraitsMappedView interface, ISimilarityTraitsMappedView interface [Remote Differential Compression],Get method, ISimilarityTraitsMappedView.Get, ISimilarityTraitsMappedView::Get, fs.isimilaritytraitsmappedview_get, msrdc/ISimilarityTraitsMappedView::Get, rdc.isimilaritytraitsmappedview_get
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RdcMappingAccessMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarityTraitsMappedView.Get
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISimilarityTraitsMappedView::Get


## -description


Returns information about the mapped view of a similarity traits table file.


## -parameters




### -param index




### -param dirty [in]

If <b>TRUE</b> is specified, the data in the currently mapped view has been changed; otherwise, the data has not changed. This parameter can be used to determine if data may need to be written to disk.


### -param numElements [in]

Minimum number of bytes of data to be mapped in the mapped view.


### -param viewInfo [out]

Pointer to a location that receives a <a href="https://msdn.microsoft.com/f7bd0ebd-6abd-4d2c-af7d-21a90a633276">SimilarityMappedViewInfo</a> structure containing information about the mapped view.


#### - fileOffset [in]

Beginning file offset, in bytes, of the underlying file data to be mapped in the mapped view.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



At least <i>numElements</i> bytes must be available in the mapped view, but depending on the application, more bytes may actually be mapped. The data must be 8-byte aligned relative to the file offset. For example, the data at file offset 0x8001 must be mapped to some memory location whose address modulo 8 is 1.




## -see-also




<a href="https://msdn.microsoft.com/48d6d4a0-fbf1-476a-b30f-83176c51cb48">ISimilarityTraitsMappedView</a>
 

 

