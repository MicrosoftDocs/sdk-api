---
UID: NF:tuner.IDVBSLocator.put_SignalPolarisation
title: IDVBSLocator::put_SignalPolarisation method
author: windows-driver-content
description: The put_SignalPolarisation method sets the signal polarisation.
old-location: mstv\idvbslocator_put_signalpolarisation.htm
old-project: mstv
ms.assetid: cc94c956-6895-451a-8d1c-2001a6fbec63
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IDVBSLocator, IDVBSLocator interface [Microsoft TV Technologies], put_SignalPolarisation method, IDVBSLocator::put_SignalPolarisation, IDVBSLocatorput_SignalPolarisation, mstv.idvbslocator_put_signalpolarisation, put_SignalPolarisation method [Microsoft TV Technologies], put_SignalPolarisation method [Microsoft TV Technologies], IDVBSLocator interface, put_SignalPolarisation,IDVBSLocator.put_SignalPolarisation, tuner/IDVBSLocator::put_SignalPolarisation
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
-	IDVBSLocator.put_SignalPolarisation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBSLocator::put_SignalPolarisation method


## -description



The <b>put_SignalPolarisation</b> method sets the signal polarisation.




## -parameters




### -param PolarisationVal [in]

Variable of type <a href="https://msdn.microsoft.com/19303d43-913f-4719-b1f8-e0e785ac0483">Polarisation</a> that specifies the signal polarisation value.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method and the associated enumeration type use the British spelling for "polarisation" to maintain consistency with standards documentation.




## -see-also




<a href="https://msdn.microsoft.com/a9f02e78-3800-4b14-81df-acab01ea072b">IDVBSLocator Interface</a>
 

 

