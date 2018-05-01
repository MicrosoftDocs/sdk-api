---
UID: NF:tuner.ITuningSpace.put_DefaultLocator
title: ITuningSpace::put_DefaultLocator method
author: windows-driver-content
description: The put_DefaultLocator method sets the default locator for this tuning space.
old-location: mstv\ituningspace_put_defaultlocator.htm
old-project: mstv
ms.assetid: 59065cc9-8a11-4551-ad3d-e7963628aa20
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ITuningSpace, ITuningSpace interface [Microsoft TV Technologies], put_DefaultLocator method, ITuningSpace::put_DefaultLocator, ITuningSpaceput_DefaultLocator, mstv.ituningspace_put_defaultlocator, put_DefaultLocator method [Microsoft TV Technologies], put_DefaultLocator method [Microsoft TV Technologies], ITuningSpace interface, put_DefaultLocator,ITuningSpace.put_DefaultLocator, tuner/ITuningSpace::put_DefaultLocator
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
-	ITuningSpace.put_DefaultLocator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpace::put_DefaultLocator method


## -description



The <b>put_DefaultLocator</b> method sets the default locator for this tuning space.




## -parameters




### -param LocatorVal






#### - pLocatorVal [in]

Pointer to the <a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a> interface of the locator object.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



See <a href="https://msdn.microsoft.com/facc14bd-182e-4b8e-a567-1bf1d3c4ff36">ITuningSpace::get_DefaultLocator</a> for more information about the default locator.

For DVB tuning spaces, the sytem type (cable, terrestrial, or satelite) of the tuning space must match the locator object. Otherwise, the method returns DISP_E_TYPEMISMATCH. For more information, see <a href="https://msdn.microsoft.com/559f882a-4d1c-4fe1-af21-b3ad7ccd3ff2">IDVBTuningSpace::put_SystemType</a>.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

