---
UID: NF:bdaiface.IBDA_NetworkProvider.UnRegisterDeviceFilter
title: IBDA_NetworkProvider::UnRegisterDeviceFilter (bdaiface.h)
description: The UnRegisterDeviceFilter method is called by BDA device filters when they are removed from the filter graph.
helpviewer_keywords: ["IBDA_NetworkProvider interface [Microsoft TV Technologies]","UnRegisterDeviceFilter method","IBDA_NetworkProvider.UnRegisterDeviceFilter","IBDA_NetworkProvider::UnRegisterDeviceFilter","IBDA_NetworkProviderUnRegisterDeviceFilter","UnRegisterDeviceFilter","UnRegisterDeviceFilter method [Microsoft TV Technologies]","UnRegisterDeviceFilter method [Microsoft TV Technologies]","IBDA_NetworkProvider interface","bdaiface/IBDA_NetworkProvider::UnRegisterDeviceFilter","mstv.ibda_networkprovider_unregisterdevicefilter"]
old-location: mstv\ibda_networkprovider_unregisterdevicefilter.htm
tech.root: mstv
ms.assetid: 7d54830f-93cc-44c0-9bb7-43c439f4aa8e
ms.date: 12/05/2018
ms.keywords: IBDA_NetworkProvider interface [Microsoft TV Technologies],UnRegisterDeviceFilter method, IBDA_NetworkProvider.UnRegisterDeviceFilter, IBDA_NetworkProvider::UnRegisterDeviceFilter, IBDA_NetworkProviderUnRegisterDeviceFilter, UnRegisterDeviceFilter, UnRegisterDeviceFilter method [Microsoft TV Technologies], UnRegisterDeviceFilter method [Microsoft TV Technologies],IBDA_NetworkProvider interface, bdaiface/IBDA_NetworkProvider::UnRegisterDeviceFilter, mstv.ibda_networkprovider_unregisterdevicefilter
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
 - IBDA_NetworkProvider::UnRegisterDeviceFilter
 - bdaiface/IBDA_NetworkProvider::UnRegisterDeviceFilter
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
 - IBDA_NetworkProvider.UnRegisterDeviceFilter
---

# IBDA_NetworkProvider::UnRegisterDeviceFilter


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>UnRegisterDeviceFilter</b> method is called by BDA device filters when they are removed from the filter graph.

## -parameters

### -param pvRegistrationContext [in]

The registration context that the filter received in the call to <b>RegisterDeviceFilter</b>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_networkprovider">IBDA_NetworkProvider Interface</a>