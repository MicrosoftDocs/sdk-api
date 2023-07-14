---
UID: NF:bdaiface.IBDA_NetworkProvider.GetSignalSource
title: IBDA_NetworkProvider::GetSignalSource (bdaiface.h)
description: The GetSignalSource method retrieves the signal source.
helpviewer_keywords: ["GetSignalSource","GetSignalSource method [Microsoft TV Technologies]","GetSignalSource method [Microsoft TV Technologies]","IBDA_NetworkProvider interface","IBDA_NetworkProvider interface [Microsoft TV Technologies]","GetSignalSource method","IBDA_NetworkProvider.GetSignalSource","IBDA_NetworkProvider::GetSignalSource","IBDA_NetworkProviderGetSignalSource","bdaiface/IBDA_NetworkProvider::GetSignalSource","mstv.ibda_networkprovider_getsignalsource"]
old-location: mstv\ibda_networkprovider_getsignalsource.htm
tech.root: mstv
ms.assetid: 943b3c1f-4aea-4c16-b730-74b63397ad9f
ms.date: 12/05/2018
ms.keywords: GetSignalSource, GetSignalSource method [Microsoft TV Technologies], GetSignalSource method [Microsoft TV Technologies],IBDA_NetworkProvider interface, IBDA_NetworkProvider interface [Microsoft TV Technologies],GetSignalSource method, IBDA_NetworkProvider.GetSignalSource, IBDA_NetworkProvider::GetSignalSource, IBDA_NetworkProviderGetSignalSource, bdaiface/IBDA_NetworkProvider::GetSignalSource, mstv.ibda_networkprovider_getsignalsource
req.header: bdaiface.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_NetworkProvider::GetSignalSource
 - bdaiface/IBDA_NetworkProvider::GetSignalSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdaiface.h
api_name:
 - IBDA_NetworkProvider.GetSignalSource
---

# IBDA_NetworkProvider::GetSignalSource


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetSignalSource</b> method retrieves the signal source.

## -parameters

### -param pulSignalSource [in, out]

Receives a value specifying the signal source.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_networkprovider">IBDA_NetworkProvider Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_networkprovider-putsignalsource">PutSignalSource</a>