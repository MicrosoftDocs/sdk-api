---
UID: NF:tuner.ITuner.EnumTuningSpaces
title: ITuner::EnumTuningSpaces (tuner.h)
description: The EnumTuningSpaces method creates a collection of tuning spaces preferred by this implementation.helpviewer_keywords: ["EnumTuningSpaces","EnumTuningSpaces method [Microsoft TV Technologies]","EnumTuningSpaces method [Microsoft TV Technologies]","ITuner interface","ITuner interface [Microsoft TV Technologies]","EnumTuningSpaces method","ITuner.EnumTuningSpaces","ITuner::EnumTuningSpaces","ITunerEnumTuningSpaces","mstv.ituner_enumtuningspaces","tuner/ITuner::EnumTuningSpaces"]
old-location: mstv\ituner_enumtuningspaces.htm
tech.root: mstv
ms.assetid: 6bd42b1b-b644-4fd7-9875-21a8d0f01243
ms.date: 12/05/2018
ms.keywords: EnumTuningSpaces, EnumTuningSpaces method [Microsoft TV Technologies], EnumTuningSpaces method [Microsoft TV Technologies],ITuner interface, ITuner interface [Microsoft TV Technologies],EnumTuningSpaces method, ITuner.EnumTuningSpaces, ITuner::EnumTuningSpaces, ITunerEnumTuningSpaces, mstv.ituner_enumtuningspaces, tuner/ITuner::EnumTuningSpaces
f1_keywords:
- tuner/ITuner.EnumTuningSpaces
dev_langs:
- c++
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
- ITuner.EnumTuningSpaces
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITuner::EnumTuningSpaces


## -description



The <b>EnumTuningSpaces</b> method creates a collection of tuning spaces preferred by this implementation.




## -parameters




### -param ppEnum [out]

Address of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumtuningspaces">IEnumTuningSpaces</a> interface pointer that will be set to the returned collection.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This list is a subset of the compatible tuning spaces for this implementation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituner">ITuner Interface</a>
 

 

