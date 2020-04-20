---
UID: NF:tuner.ILocator.get_OuterFECRate
title: ILocator::get_OuterFECRate (tuner.h)
description: The get_OuterFECRate method gets the outer FEC rate.helpviewer_keywords: ["IDigitalLocatorget_OuterFECRate","ILocator interface [Microsoft TV Technologies]","get_OuterFECRate method","ILocator.get_OuterFECRate","ILocator::get_OuterFECRate","get_OuterFECRate","get_OuterFECRate method [Microsoft TV Technologies]","get_OuterFECRate method [Microsoft TV Technologies]","ILocator interface","mstv.ilocator_get_outerfecrate","tuner/ILocator::get_OuterFECRate"]
old-location: mstv\ilocator_get_outerfecrate.htm
tech.root: mstv
ms.assetid: 550103a8-dcf9-4a52-817a-61a589de4299
ms.date: 12/05/2018
ms.keywords: IDigitalLocatorget_OuterFECRate, ILocator interface [Microsoft TV Technologies],get_OuterFECRate method, ILocator.get_OuterFECRate, ILocator::get_OuterFECRate, get_OuterFECRate, get_OuterFECRate method [Microsoft TV Technologies], get_OuterFECRate method [Microsoft TV Technologies],ILocator interface, mstv.ilocator_get_outerfecrate, tuner/ILocator::get_OuterFECRate
f1_keywords:
- tuner/ILocator.get_OuterFECRate
dev_langs:
- c++
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
- ILocator.get_OuterFECRate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILocator::get_OuterFECRate


## -description



The <b>get_OuterFECRate</b> method gets the outer FEC rate.




## -parameters




### -param FEC [out]

Pointer to a variable of type <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/binaryconvolutioncoderate">BinaryConvolutionCodeRate</a> that receives the outer FEC rate.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a>



<a href="https://docs.microsoft.com/previous-versions/dd693581(v=vs.85)">get_InnerFECRate</a>



<a href="https://docs.microsoft.com/previous-versions/dd693582(v=vs.85)">get_OuterFEC</a>



<a href="https://docs.microsoft.com/previous-versions/dd693588(v=vs.85)">put_OuterFECRate</a>
 

 

