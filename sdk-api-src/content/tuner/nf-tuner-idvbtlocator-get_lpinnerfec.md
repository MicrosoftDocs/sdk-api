---
UID: NF:tuner.IDVBTLocator.get_LPInnerFEC
title: IDVBTLocator::get_LPInnerFEC method
author: windows-driver-content
description: The get_LPInnerFEC method retrieves the inner FEC type of the low-priority stream.
old-location: mstv\idvbtlocator_get_lpinnerfec.htm
old-project: mstv
ms.assetid: 069904ad-5faa-4ac4-bf30-538284de2de8
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IDVBTLocator, IDVBTLocator interface [Microsoft TV Technologies], get_LPInnerFEC method, IDVBTLocator::get_LPInnerFEC, IDVBTLocatorget_LPInnerFEC, get_LPInnerFEC method [Microsoft TV Technologies], get_LPInnerFEC method [Microsoft TV Technologies], IDVBTLocator interface, get_LPInnerFEC,IDVBTLocator.get_LPInnerFEC, mstv.idvbtlocator_get_lpinnerfec, tuner/IDVBTLocator::get_LPInnerFEC
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IDVBTLocator.get_LPInnerFEC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBTLocator::get_LPInnerFEC method


## -description



The <b>get_LPInnerFEC</b> method retrieves the inner FEC type of the low-priority stream.




## -parameters




### -param FEC






#### - pFEC [out]

Receives a member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559594">FECMethod</a> enumeration.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/f5a95a68-fee0-404c-b9c6-6b808977f8d2">IDVBTLocator Interface</a>
 

 

