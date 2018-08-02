---
UID: NF:tuner.IDVBTLocator.get_Bandwidth
title: IDVBTLocator::get_Bandwidth
author: windows-sdk-content
description: The get_Bandwidth method retrieves the bandwidth of the frequency.
old-location: mstv\idvbtlocator_get_bandwidth.htm
old-project: mstv
ms.assetid: 7483d876-fdcc-4eee-b4f3-338846a159c0
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],get_Bandwidth method, IDVBTLocator.get_Bandwidth, IDVBTLocator::get_Bandwidth, IDVBTLocatorget_Bandwidth, get_Bandwidth, get_Bandwidth method [Microsoft TV Technologies], get_Bandwidth method [Microsoft TV Technologies],IDVBTLocator interface, mstv.idvbtlocator_get_bandwidth, tuner/IDVBTLocator::get_Bandwidth
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IDVBTLocator.get_Bandwidth
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBTLocator::get_Bandwidth


## -description



The <b>get_Bandwidth</b> method retrieves the bandwidth of the frequency.




## -parameters




### -param BandWidthVal






#### - pBandWidthVal [out]

Receives the bandwidth, in megahertz (MHz).


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The bandwidth is determined by the bandwidth field in the DVB terrestrial delivery system descriptor, as defined in EN 300 468. Valid values are 7 or 8.




## -see-also




<a href="https://msdn.microsoft.com/f5a95a68-fee0-404c-b9c6-6b808977f8d2">IDVBTLocator Interface</a>
 

 

