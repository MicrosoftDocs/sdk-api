---
UID: NF:strmif.IAMExtTransport.GetBump
title: IAMExtTransport::GetBump (strmif.h)
description: The GetBump method retrieves the status of bump mode.
helpviewer_keywords: ["GetBump","GetBump method [DirectShow]","GetBump method [DirectShow]","IAMExtTransport interface","IAMExtTransport interface [DirectShow]","GetBump method","IAMExtTransport.GetBump","IAMExtTransport::GetBump","IAMExtTransportGetBump","dshow.iamexttransport_getbump","strmif/IAMExtTransport::GetBump"]
old-location: dshow\iamexttransport_getbump.htm
tech.root: dshow
ms.assetid: 340b7c9a-cfd9-4915-b0fc-0d12d7663578
ms.date: 12/05/2018
ms.keywords: GetBump, GetBump method [DirectShow], GetBump method [DirectShow],IAMExtTransport interface, IAMExtTransport interface [DirectShow],GetBump method, IAMExtTransport.GetBump, IAMExtTransport::GetBump, IAMExtTransportGetBump, dshow.iamexttransport_getbump, strmif/IAMExtTransport::GetBump
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMExtTransport::GetBump
 - strmif/IAMExtTransport::GetBump
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMExtTransport.GetBump
---

# IAMExtTransport::GetBump


## -description

The <code>GetBump</code> method retrieves the status of bump mode.



This method is not implemented.

## -parameters

### -param pSpeed [out]

Pointer to a <b>long</b> integer that receives the temporary bump speed, as a multiple of normal speed.

### -param pDuration [out]

Pointer to a <b>long</b> integer that receives the duration of a bump. The duration is given in the current time format; see <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-settransportbasicparameters">IAMExtTransport::SetTransportBasicParameters</a> for more information.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

This method returns the temporary speed and remaining duration for an active "bump."

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="/windows/desktop/DirectShow/msdv-driver">MSDV</a> does not support this method. It returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-setbump">IAMExtTransport::SetBump</a>