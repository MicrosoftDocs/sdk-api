---
UID: NF:bdaiface.IBDA_NetworkProvider.RegisterDeviceFilter
title: IBDA_NetworkProvider::RegisterDeviceFilter (bdaiface.h)
description: The RegisterDeviceFilter method is called by a BDA device filter to register itself in the filter graph.
helpviewer_keywords: ["IBDA_NetworkProvider interface [Microsoft TV Technologies]","RegisterDeviceFilter method","IBDA_NetworkProvider.RegisterDeviceFilter","IBDA_NetworkProvider::RegisterDeviceFilter","IBDA_NetworkProviderRegisterDeviceFilter","RegisterDeviceFilter","RegisterDeviceFilter method [Microsoft TV Technologies]","RegisterDeviceFilter method [Microsoft TV Technologies]","IBDA_NetworkProvider interface","bdaiface/IBDA_NetworkProvider::RegisterDeviceFilter","mstv.ibda_networkprovider_registerdevicefilter"]
old-location: mstv\ibda_networkprovider_registerdevicefilter.htm
tech.root: mstv
ms.assetid: 88050024-5960-4ce5-8645-82db3e17b12c
ms.date: 12/05/2018
ms.keywords: IBDA_NetworkProvider interface [Microsoft TV Technologies],RegisterDeviceFilter method, IBDA_NetworkProvider.RegisterDeviceFilter, IBDA_NetworkProvider::RegisterDeviceFilter, IBDA_NetworkProviderRegisterDeviceFilter, RegisterDeviceFilter, RegisterDeviceFilter method [Microsoft TV Technologies], RegisterDeviceFilter method [Microsoft TV Technologies],IBDA_NetworkProvider interface, bdaiface/IBDA_NetworkProvider::RegisterDeviceFilter, mstv.ibda_networkprovider_registerdevicefilter
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
 - IBDA_NetworkProvider::RegisterDeviceFilter
 - bdaiface/IBDA_NetworkProvider::RegisterDeviceFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_NetworkProvider.RegisterDeviceFilter
---

# IBDA_NetworkProvider::RegisterDeviceFilter


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>RegisterDeviceFilter</b> method is called by a BDA device filter to register itself in the filter graph.

## -parameters

### -param pUnkFilterControl [in]

Pointer to the filter's <b>IUnknown</b> interface.

### -param ppvRegisitrationContext [out]

Pointer that receives the registration context. The filter should store this value and return it in the call to <b>UnRegisterDeviceFilter</b>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_networkprovider">IBDA_NetworkProvider Interface</a>