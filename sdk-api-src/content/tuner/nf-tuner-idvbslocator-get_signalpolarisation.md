---
UID: NF:tuner.IDVBSLocator.get_SignalPolarisation
title: IDVBSLocator::get_SignalPolarisation
author: windows-sdk-content
description: The get_SignalPolarisation method retrieves the signal polarisation.
old-location: mstv\idvbslocator_get_signalpolarisation.htm
old-project: mstv
ms.assetid: adb9d7b6-5876-4b3f-9d82-f5e740feb1eb
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDVBSLocator interface [Microsoft TV Technologies],get_SignalPolarisation method, IDVBSLocator.get_SignalPolarisation, IDVBSLocator::get_SignalPolarisation, IDVBSLocatorget_SignalPolarisation, get_SignalPolarisation, get_SignalPolarisation method [Microsoft TV Technologies], get_SignalPolarisation method [Microsoft TV Technologies],IDVBSLocator interface, mstv.idvbslocator_get_signalpolarisation, tuner/IDVBSLocator::get_SignalPolarisation
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
 - IDVBSLocator.get_SignalPolarisation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBSLocator::get_SignalPolarisation


## -description



The <b>get_SignalPolarisation</b> method retrieves the signal polarisation.




## -parameters




### -param PolarisationVal






#### - pPolarisationVal [out]

Pointer to a variable of type <a href="https://msdn.microsoft.com/19303d43-913f-4719-b1f8-e0e785ac0483">Polarisation</a> that receives the polarisation value.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method and the associated enumeration type use the British spelling for "polarisation" to maintain consistency with standards documentation.




## -see-also




<a href="https://msdn.microsoft.com/a9f02e78-3800-4b14-81df-acab01ea072b">IDVBSLocator Interface</a>
 

 

