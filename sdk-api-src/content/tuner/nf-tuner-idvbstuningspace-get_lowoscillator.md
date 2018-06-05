---
UID: NF:tuner.IDVBSTuningSpace.get_LowOscillator
title: IDVBSTuningSpace::get_LowOscillator
author: windows-sdk-content
description: The get_LowOscillator method retrieves the low oscillator frequency.
old-location: mstv\idvbstuningspace_get_lowoscillator.htm
old-project: mstv
ms.assetid: 7f48902d-9242-4791-b0f1-fc4ab5bd85c0
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDVBSTuningSpace interface [Microsoft TV Technologies],get_LowOscillator method, IDVBSTuningSpace.get_LowOscillator, IDVBSTuningSpace::get_LowOscillator, IDVBSTuningSpaceget_LowOscillator, get_LowOscillator, get_LowOscillator method [Microsoft TV Technologies], get_LowOscillator method [Microsoft TV Technologies],IDVBSTuningSpace interface, mstv.idvbstuningspace_get_lowoscillator, tuner/IDVBSTuningSpace::get_LowOscillator
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IDVBSTuningSpace.get_LowOscillator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBSTuningSpace::get_LowOscillator


## -description



The <b>get_LowOscillator</b> method retrieves the low oscillator frequency.




## -parameters




### -param LowOscillator






#### - pLowOscillator [out]

Receives the low oscillator frequency, in kilohertz (kHz).


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/46c143d7-b9ec-4808-a4d2-337e6e0252dd">IDVBSTuningSpace Interface</a>
 

 

