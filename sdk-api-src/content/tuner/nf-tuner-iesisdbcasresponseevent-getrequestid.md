---
UID: NF:tuner.IESIsdbCasResponseEvent.GetRequestId
title: IESIsdbCasResponseEvent::GetRequestId
author: windows-driver-content
description: Gets the request identifier returned in an IsdbCasResponse event. The request identifier identifies the request originated by a PBDA media sink device (MSD).
old-location: mstv\iesisdbcasresponseevent_getrequestid.htm
old-project: mstv
ms.assetid: b3ab39b4-567f-49a5-b3d2-460ec648ab26
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetRequestId, GetRequestId method [DirectShow], GetRequestId method [DirectShow],IESIsdbCasResponseEvent interface, IESIsdbCasResponseEvent interface [DirectShow],GetRequestId method, IESIsdbCasResponseEvent.GetRequestId, IESIsdbCasResponseEvent::GetRequestId, mstv.iesisdbcasresponseevent_getrequestid, tuner/IESIsdbCasResponseEvent::GetRequestId
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
-	IESIsdbCasResponseEvent.GetRequestId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESIsdbCasResponseEvent::GetRequestId


## -description


Gets the request identifier returned in an <a href="https://msdn.microsoft.com/141c6798-5dca-495e-bdbe-f07e457a3d8a">IsdbCasResponse</a> event. The request identifier identifies the request originated by a PBDA media sink device (MSD).


## -parameters




### -param pRequestId [out, retval]

Receives the request identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/141c6798-5dca-495e-bdbe-f07e457a3d8a">IESIsdbCasResponseEvent</a>
 

 

