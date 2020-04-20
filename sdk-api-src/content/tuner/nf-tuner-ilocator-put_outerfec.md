---
UID: NF:tuner.ILocator.put_OuterFEC
title: ILocator::put_OuterFEC (tuner.h)
description: The put_OuterFEC method sets the type of outer FEC to use.helpviewer_keywords: ["IDigitalLocatorput_OuterFEC","ILocator interface [Microsoft TV Technologies]","put_OuterFEC method","ILocator.put_OuterFEC","ILocator::put_OuterFEC","mstv.ilocator_put_outerfec","put_OuterFEC","put_OuterFEC method [Microsoft TV Technologies]","put_OuterFEC method [Microsoft TV Technologies]","ILocator interface","tuner/ILocator::put_OuterFEC"]
old-location: mstv\ilocator_put_outerfec.htm
tech.root: mstv
ms.assetid: 0aaa4d8e-e760-4e22-90fe-e5667fafa113
ms.date: 12/05/2018
ms.keywords: IDigitalLocatorput_OuterFEC, ILocator interface [Microsoft TV Technologies],put_OuterFEC method, ILocator.put_OuterFEC, ILocator::put_OuterFEC, mstv.ilocator_put_outerfec, put_OuterFEC, put_OuterFEC method [Microsoft TV Technologies], put_OuterFEC method [Microsoft TV Technologies],ILocator interface, tuner/ILocator::put_OuterFEC
f1_keywords:
- tuner/ILocator.put_OuterFEC
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
- ILocator.put_OuterFEC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILocator::put_OuterFEC


## -description



The <b>put_OuterFEC</b> method sets the type of outer FEC to use.




## -parameters




### -param FEC [in]

Specifies the outer FEC. This parameter is a value of type <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/fecmethod">FECMethod</a>.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a>



<a href="https://docs.microsoft.com/previous-versions/dd693582(v=vs.85)">get_OuterFEC</a>



<a href="https://docs.microsoft.com/previous-versions/dd693585(v=vs.85)">put_InnerFEC</a>



<a href="https://docs.microsoft.com/previous-versions/dd693588(v=vs.85)">put_OuterFECRate</a>
 

 

