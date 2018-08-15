---
UID: NF:tuner.IESIsdbCasResponseEvent.GetDataLength
title: IESIsdbCasResponseEvent::GetDataLength
author: windows-sdk-content
description: Gets the length of response data returned in anIsdbCasResponse event.
old-location: mstv\iesisdbcasresponseevent_getdatalength.htm
old-project: mstv
ms.assetid: dc625c6f-84e8-4a82-b53c-717b33c10d04
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetDataLength, GetDataLength method [DirectShow], GetDataLength method [DirectShow],IESIsdbCasResponseEvent interface, IESIsdbCasResponseEvent interface [DirectShow],GetDataLength method, IESIsdbCasResponseEvent.GetDataLength, IESIsdbCasResponseEvent::GetDataLength, mstv.iesisdbcasresponseevent_getdatalength, tuner/IESIsdbCasResponseEvent::GetDataLength
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
 - IESIsdbCasResponseEvent.GetDataLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESIsdbCasResponseEvent::GetDataLength


## -description


Gets the length of response data returned in an<a href="https://msdn.microsoft.com/141c6798-5dca-495e-bdbe-f07e457a3d8a">IsdbCasResponse</a> event.


## -parameters




### -param pRequestLength [out, retval]

Receives the length of the response data, in bytes.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/141c6798-5dca-495e-bdbe-f07e457a3d8a">IESIsdbCasResponseEvent</a>
 

 

