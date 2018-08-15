---
UID: NF:tuner.IESIsdbCasResponseEvent.GetRequestId
title: IESIsdbCasResponseEvent::GetRequestId
author: windows-sdk-content
description: Gets the request identifier returned in an IsdbCasResponse event. The request identifier identifies the request originated by a PBDA media sink device (MSD).
old-location: mstv\iesisdbcasresponseevent_getrequestid.htm
old-project: mstv
ms.assetid: b3ab39b4-567f-49a5-b3d2-460ec648ab26
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetRequestId, GetRequestId method [DirectShow], GetRequestId method [DirectShow],IESIsdbCasResponseEvent interface, IESIsdbCasResponseEvent interface [DirectShow],GetRequestId method, IESIsdbCasResponseEvent.GetRequestId, IESIsdbCasResponseEvent::GetRequestId, mstv.iesisdbcasresponseevent_getrequestid, tuner/IESIsdbCasResponseEvent::GetRequestId
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESIsdbCasResponseEvent.GetRequestId
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
 

 

