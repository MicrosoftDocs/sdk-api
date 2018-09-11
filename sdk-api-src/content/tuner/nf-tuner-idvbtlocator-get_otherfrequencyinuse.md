---
UID: NF:tuner.IDVBTLocator.get_OtherFrequencyInUse
title: IDVBTLocator::get_OtherFrequencyInUse
author: windows-sdk-content
description: The get_OtherFrequencyInUse method indicates whether the frequency is being used by another DVB-T broadcaster.
old-location: mstv\idvbtlocator_get_otherfrequencyinuse.htm
tech.root: mstv
ms.assetid: fcb39760-901f-4c62-a517-bee7ea96f8d9
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],get_OtherFrequencyInUse method, IDVBTLocator.get_OtherFrequencyInUse, IDVBTLocator::get_OtherFrequencyInUse, IDVBTLocatorget_OtherFrequencyInUse, get_OtherFrequencyInUse, get_OtherFrequencyInUse method [Microsoft TV Technologies], get_OtherFrequencyInUse method [Microsoft TV Technologies],IDVBTLocator interface, mstv.idvbtlocator_get_otherfrequencyinuse, tuner/IDVBTLocator::get_OtherFrequencyInUse
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IDVBTLocator.get_OtherFrequencyInUse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVBTLocator::get_OtherFrequencyInUse


## -description



The <b>get_OtherFrequencyInUse</b> method indicates whether the frequency is being used by another DVB-T broadcaster.




## -parameters




### -param OtherFrequencyInUseVal

TBD




#### - pOtherFrequencyInUseVal [out]

Receives that value VARIANT_TRUE if the frequency is being used by another DVB-T broadcaster, or VARIANT_FALSE otherwise.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/f5a95a68-fee0-404c-b9c6-6b808977f8d2">IDVBTLocator Interface</a>
 

 

