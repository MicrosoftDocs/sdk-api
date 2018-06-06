---
UID: NF:tuner.IDVBSTuningSpace.get_HighOscillator
title: IDVBSTuningSpace::get_HighOscillator
author: windows-sdk-content
description: The get_HighOscillator method retrieves the high oscillator frequency.
old-location: mstv\idvbstuningspace_get_highoscillator.htm
old-project: mstv
ms.assetid: e3b70684-5066-411e-9946-ccfc1efa3e7c
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDVBSTuningSpace interface [Microsoft TV Technologies],get_HighOscillator method, IDVBSTuningSpace.get_HighOscillator, IDVBSTuningSpace::get_HighOscillator, IDVBSTuningSpaceget_HighOscillator, get_HighOscillator, get_HighOscillator method [Microsoft TV Technologies], get_HighOscillator method [Microsoft TV Technologies],IDVBSTuningSpace interface, mstv.idvbstuningspace_get_highoscillator, tuner/IDVBSTuningSpace::get_HighOscillator
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
 - IDVBSTuningSpace.get_HighOscillator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBSTuningSpace::get_HighOscillator


## -description



The <b>get_HighOscillator</b> method retrieves the high oscillator frequency.




## -parameters




### -param HighOscillator






#### - pHighOscillator [out]

Receives the high oscillator frequency, in kilohertz (kHz).


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/46c143d7-b9ec-4808-a4d2-337e6e0252dd">IDVBSTuningSpace Interface</a>
 

 

