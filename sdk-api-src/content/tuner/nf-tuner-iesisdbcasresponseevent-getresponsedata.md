---
UID: NF:tuner.IESIsdbCasResponseEvent.GetResponseData
title: IESIsdbCasResponseEvent::GetResponseData
author: windows-driver-content
description: Gets the response data returned in an IsdbCasResponse event.
old-location: mstv\iesisdbcasresponseevent_getresponsedata.htm
old-project: mstv
ms.assetid: ee0618a6-6162-4178-be44-978558add914
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetResponseData, GetResponseData method [DirectShow], GetResponseData method [DirectShow],IESIsdbCasResponseEvent interface, IESIsdbCasResponseEvent interface [DirectShow],GetResponseData method, IESIsdbCasResponseEvent.GetResponseData, IESIsdbCasResponseEvent::GetResponseData, mstv.iesisdbcasresponseevent_getresponsedata, tuner/IESIsdbCasResponseEvent::GetResponseData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IESIsdbCasResponseEvent.GetResponseData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESIsdbCasResponseEvent::GetResponseData


## -description


Gets the response data returned in an <a href="https://msdn.microsoft.com/141c6798-5dca-495e-bdbe-f07e457a3d8a">IsdbCasResponse</a> event.


## -parameters




### -param pbData [out, retval]

Pointer to a buffer that receives the response data. The caller must free this memory after use.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/141c6798-5dca-495e-bdbe-f07e457a3d8a">IESIsdbCasResponseEvent</a>
 

 

