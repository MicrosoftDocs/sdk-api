---
UID: NF:tuner.IDVBTLocator.put_LPInnerFEC
title: IDVBTLocator::put_LPInnerFEC method
author: windows-driver-content
description: The put_LPInnerFEC method sets the inner FEC type of the low-priority stream.
old-location: mstv\idvbtlocator_put_lpinnerfec.htm
old-project: mstv
ms.assetid: 37b5b063-a0ae-4ef8-a63b-44c009a31eb8
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IDVBTLocator, IDVBTLocator interface [Microsoft TV Technologies], put_LPInnerFEC method, IDVBTLocator::put_LPInnerFEC, IDVBTLocatorput_LPInnerFEC, mstv.idvbtlocator_put_lpinnerfec, put_LPInnerFEC method [Microsoft TV Technologies], put_LPInnerFEC method [Microsoft TV Technologies], IDVBTLocator interface, put_LPInnerFEC,IDVBTLocator.put_LPInnerFEC, tuner/IDVBTLocator::put_LPInnerFEC
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
-	IDVBTLocator.put_LPInnerFEC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBTLocator::put_LPInnerFEC method


## -description



The <b>put_LPInnerFEC</b> method sets the inner FEC type of the low-priority stream.




## -parameters




### -param FEC [in]

Variable of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff559594">FECMethod</a> that specifies the FEC type.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/f5a95a68-fee0-404c-b9c6-6b808977f8d2">IDVBTLocator Interface</a>
 

 

