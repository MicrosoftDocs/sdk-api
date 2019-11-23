---
UID: NF:bdatif.IBDA_TIF_REGISTRATION.RegisterTIFEx
title: IBDA_TIF_REGISTRATION::RegisterTIFEx (bdatif.h)

description: The RegisterTIFEx method registers a Transport Information Filter (TIF) with the Network Provider.
old-location: mstv\ibda_tif_registration_registertifex.htm
tech.root: mstv
ms.assetid: 1cfc653f-b552-4f38-9ca1-457ab4de3598

ms.date: 12/05/2018
ms.keywords: IBDA_TIF_REGISTRATION interface [Microsoft TV Technologies],RegisterTIFEx method, IBDA_TIF_REGISTRATION.RegisterTIFEx, IBDA_TIF_REGISTRATION::RegisterTIFEx, IBDA_TIF_REGISTRATIONRegisterTIFEx, RegisterTIFEx, RegisterTIFEx method [Microsoft TV Technologies], RegisterTIFEx method [Microsoft TV Technologies],IBDA_TIF_REGISTRATION interface, bdatif/IBDA_TIF_REGISTRATION::RegisterTIFEx, mstv.ibda_tif_registration_registertifex
ms.topic: method
f1_keywords: 
 - "bdatif/IBDA_TIF_REGISTRATION.RegisterTIFEx"
dev_langs:
 - c++
req.header: bdatif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - bdatif.h
api_name:
 - IBDA_TIF_REGISTRATION.RegisterTIFEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_TIF_REGISTRATION::RegisterTIFEx


## -description



The <b>RegisterTIFEx</b> method registers a Transport Information Filter (TIF) with the Network Provider.




## -parameters




### -param pTIFInputPin [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface of the input pin on the TIF.


### -param ppvRegistrationContext [in, out]

Receives a token identifying the connection. Pass this token in the <b>UnregisterTIF</b> method when the TIF unregisters itself.


### -param ppMpeg2DataControl [in, out]

Receives a pointer to an <b>IUnknown</b> interface, which the TIF queries for the <a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-impeg2pidmap">IMPEG2PIDMap</a> interface. It uses the <b>IMPEG2PIDMap</b> to map and unmap PID values.


## -returns



The method returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nn-bdatif-ibda_tif_registration">IBDA_TIF_REGISTRATION Interface</a>
 

 

