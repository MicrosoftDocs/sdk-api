---
UID: NF:tuner.IDVBTLocator.put_Bandwidth
title: IDVBTLocator::put_Bandwidth (tuner.h)
description: The put_BandWidth method sets the bandwidth of the frequency.helpviewer_keywords: ["IDVBTLocator interface [Microsoft TV Technologies]","put_Bandwidth method","IDVBTLocator.put_Bandwidth","IDVBTLocator::put_Bandwidth","IDVBTLocatorput_Bandwidth","mstv.idvbtlocator_put_bandwidth","put_Bandwidth","put_Bandwidth method [Microsoft TV Technologies]","put_Bandwidth method [Microsoft TV Technologies]","IDVBTLocator interface","tuner/IDVBTLocator::put_Bandwidth"]
old-location: mstv\idvbtlocator_put_bandwidth.htm
tech.root: mstv
ms.assetid: a842e905-cd4a-4d62-a9da-153832e44382
ms.date: 12/05/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],put_Bandwidth method, IDVBTLocator.put_Bandwidth, IDVBTLocator::put_Bandwidth, IDVBTLocatorput_Bandwidth, mstv.idvbtlocator_put_bandwidth, put_Bandwidth, put_Bandwidth method [Microsoft TV Technologies], put_Bandwidth method [Microsoft TV Technologies],IDVBTLocator interface, tuner/IDVBTLocator::put_Bandwidth
f1_keywords:
- tuner/IDVBTLocator.put_Bandwidth
dev_langs:
- c++
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
- IDVBTLocator.put_Bandwidth
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVBTLocator::put_Bandwidth


## -description



The <b>put_BandWidth</b> method sets the bandwidth of the frequency.




## -parameters




### -param BandwidthVal [in]

Specifies the bandwidth, in megahertz (MHz). The value should be taken from the bandwidth field in the terrestrial delivery system descriptor.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtlocator">IDVBTLocator Interface</a>
 

 

