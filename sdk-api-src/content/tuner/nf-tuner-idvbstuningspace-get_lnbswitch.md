---
UID: NF:tuner.IDVBSTuningSpace.get_LNBSwitch
title: IDVBSTuningSpace::get_LNBSwitch method
author: windows-driver-content
description: The get_LNBSwitch method retrieves the LNB switch.
old-location: mstv\idvbstuningspace_get_lnbswitch.htm
old-project: mstv
ms.assetid: 56cea4ef-7679-4b78-883d-194c9259032f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IDVBSTuningSpace, IDVBSTuningSpace interface [Microsoft TV Technologies], get_LNBSwitch method, IDVBSTuningSpace::get_LNBSwitch, IDVBSTuningSpaceget_LNBSwitch, get_LNBSwitch method [Microsoft TV Technologies], get_LNBSwitch method [Microsoft TV Technologies], IDVBSTuningSpace interface, get_LNBSwitch,IDVBSTuningSpace.get_LNBSwitch, mstv.idvbstuningspace_get_lnbswitch, tuner/IDVBSTuningSpace::get_LNBSwitch
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
-	IDVBSTuningSpace.get_LNBSwitch
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBSTuningSpace::get_LNBSwitch method


## -description



The <b>get_LNBSwitch</b> method retrieves the LNB switch.




## -parameters




### -param LNBSwitch






#### - pLNBSwitch [out]

Receives the LNB switch frequency, in kilohertz (kHz).


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/46c143d7-b9ec-4808-a4d2-337e6e0252dd">IDVBSTuningSpace Interface</a>
 

 

