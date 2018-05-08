---
UID: NF:tuner.ILocator.get_InnerFECRate
title: ILocator::get_InnerFECRate
author: windows-driver-content
description: The get_InnerFECRate method gets the inner FEC rate.
old-location: mstv\ilocator_get_innerfecrate.htm
old-project: mstv
ms.assetid: d9600c31-9a95-4955-8f8c-542760631050
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IDigitalLocatorget_InnerFECRate, ILocator interface [Microsoft TV Technologies],get_InnerFECRate method, ILocator.get_InnerFECRate, ILocator::get_InnerFECRate, get_InnerFECRate, get_InnerFECRate method [Microsoft TV Technologies], get_InnerFECRate method [Microsoft TV Technologies],ILocator interface, mstv.ilocator_get_innerfecrate, tuner/ILocator::get_InnerFECRate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
-	ILocator.get_InnerFECRate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ILocator::get_InnerFECRate


## -description



The <b>get_InnerFECRate</b> method gets the inner FEC rate.




## -parameters




### -param FEC [out]

Pointer to a variable of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff556566">BinaryConvolutionCodeRate</a> that receives the inner FEC rate.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a>



<a href="mstv.idigitallocator_get_innerfec">get_InnerFEC</a>



<a href="mstv.idigitallocator_get_outerfecrate">get_OuterFECRate</a>



<a href="mstv.idigitallocator_put_innerfecrate">put_InnerFECRate</a>
 

 

