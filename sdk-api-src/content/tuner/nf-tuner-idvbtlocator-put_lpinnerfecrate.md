---
UID: NF:tuner.IDVBTLocator.put_LPInnerFECRate
title: IDVBTLocator::put_LPInnerFECRate (tuner.h)
author: windows-sdk-content
description: The put_LPInnerFECRate method sets the inner FEC rate of the low-priority stream.
old-location: mstv\idvbtlocator_put_lpinnerfecrate.htm
tech.root: mstv
ms.assetid: 4fcce13b-1cc4-4ee7-b010-2c5ffd55a5f7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],put_LPInnerFECRate method, IDVBTLocator.put_LPInnerFECRate, IDVBTLocator::put_LPInnerFECRate, IDVBTLocatorput_LPInnerFECRate, mstv.idvbtlocator_put_lpinnerfecrate, put_LPInnerFECRate, put_LPInnerFECRate method [Microsoft TV Technologies], put_LPInnerFECRate method [Microsoft TV Technologies],IDVBTLocator interface, tuner/IDVBTLocator::put_LPInnerFECRate
ms.topic: method
f1_keywords: ["tuner/IDVBTLocator.put_LPInnerFECRate"]
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
 - IDVBTLocator.put_LPInnerFECRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVBTLocator::put_LPInnerFECRate


## -description



The <b>put_LPInnerFECRate</b> method sets the inner FEC rate of the low-priority stream.




## -parameters




### -param FEC [in]

Variable of type <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/binaryconvolutioncoderate">BinaryConvolutionCodeRate</a> that specifies the rate.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtlocator">IDVBTLocator Interface</a>
 

 

