---
UID: NF:tuner.IESValueUpdatedEvent.GetValueNames
title: IESValueUpdatedEvent::GetValueNames (tuner.h)
description: For a name-value pair in the PBDA General Purpose Name-Value Service, gets the name for the value that has been updated.
helpviewer_keywords: ["GetValueNames","GetValueNames method [Microsoft TV Technologies]","GetValueNames method [Microsoft TV Technologies]","IESValueUpdatedEvent interface","IESValueUpdatedEvent interface [Microsoft TV Technologies]","GetValueNames method","IESValueUpdatedEvent.GetValueNames","IESValueUpdatedEvent::GetValueNames","mstv.iesvalueupdatedevent_getvaluenames","tuner/IESValueUpdatedEvent::GetValueNames"]
old-location: mstv\iesvalueupdatedevent_getvaluenames.htm
tech.root: mstv
ms.assetid: bc008b4a-fa6f-4b62-90da-417813081344
ms.date: 12/05/2018
ms.keywords: GetValueNames, GetValueNames method [Microsoft TV Technologies], GetValueNames method [Microsoft TV Technologies],IESValueUpdatedEvent interface, IESValueUpdatedEvent interface [Microsoft TV Technologies],GetValueNames method, IESValueUpdatedEvent.GetValueNames, IESValueUpdatedEvent::GetValueNames, mstv.iesvalueupdatedevent_getvaluenames, tuner/IESValueUpdatedEvent::GetValueNames
f1_keywords:
- tuner/IESValueUpdatedEvent.GetValueNames
dev_langs:
- c++
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
- IESValueUpdatedEvent.GetValueNames
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESValueUpdatedEvent::GetValueNames


## -description


For a name-value pair in the PBDA General Purpose Name-Value Service, gets the name for the value that has been updated. PBDA Media Sink Devices (MSDs) get this name from <b>ValueUpdated</b> events fired by Media Transform Devices (MTDs) that implement the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iesvalueupdatedevent">IESValueUpdatedEvent</a> interface.


## -parameters




### -param pbstrNames [out, retval]

Pointer to a buffer that gets the name that has been updated. The caller is responsible for freeing this memory.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iesvalueupdatedevent">IESValueUpdatedEvent</a>
 

 

