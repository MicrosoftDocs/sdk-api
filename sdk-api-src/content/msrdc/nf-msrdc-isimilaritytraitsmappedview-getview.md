---
UID: NF:msrdc.ISimilarityTraitsMappedView.GetView
title: ISimilarityTraitsMappedView::GetView method
author: windows-driver-content
description: Returns the beginning and ending addresses for the mapped view of a similarity traits table file.
old-location: rdc\isimilaritytraitsmappedview_getview.htm
old-project: Rdc
ms.assetid: ac229f59-eb2f-471e-9f31-0e7139becdcb
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetView method [Remote Differential Compression], GetView method [Remote Differential Compression], ISimilarityTraitsMappedView interface, GetView,ISimilarityTraitsMappedView.GetView, ISimilarityTraitsMappedView, ISimilarityTraitsMappedView interface [Remote Differential Compression], GetView method, ISimilarityTraitsMappedView::GetView, fs.isimilaritytraitsmappedview_getview, msrdc/ISimilarityTraitsMappedView::GetView, rdc.isimilaritytraitsmappedview_getview
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: RdcMappingAccessMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsRdc.dll
api_name:
-	ISimilarityTraitsMappedView.GetView
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISimilarityTraitsMappedView::GetView method


## -description


Returns the beginning and ending addresses for the mapped view of a similarity traits table file.


## -parameters




### -param mappedPageBegin [out]

Pointer to a location that receives the start of the data that is mapped for this view.


### -param mappedPageEnd [out]

Pointer to a location that receives the end of the data that is mapped for this view, plus one.


## -returns



This method does not return a value.




## -remarks



If there is no mapped view, then <code>*mappedPageBegin</code> must be set to zero. Otherwise, <code>*mappedPageBegin</code> is set to a valid pointer, and <code>*mappedPageBegin - *mappedPageEnd</code> equals the size, in bytes, of the mapped area.




## -see-also




<a href="https://msdn.microsoft.com/48d6d4a0-fbf1-476a-b30f-83176c51cb48">ISimilarityTraitsMappedView</a>
 

 

