---
UID: NF:strmif.IAMExtTransport.SetBump
title: IAMExtTransport::SetBump (strmif.h)
description: The SetBump method temporarily changes the playback, for synchronization of multiple external devices.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","SetBump method","IAMExtTransport.SetBump","IAMExtTransport::SetBump","IAMExtTransportSetBump","SetBump","SetBump method [DirectShow]","SetBump method [DirectShow]","IAMExtTransport interface","dshow.iamexttransport_setbump","strmif/IAMExtTransport::SetBump"]
old-location: dshow\iamexttransport_setbump.htm
tech.root: dshow
ms.assetid: c2f2b59f-2522-4f13-8861-fb4e2d9d406c
ms.date: 12/05/2018
ms.keywords: IAMExtTransport interface [DirectShow],SetBump method, IAMExtTransport.SetBump, IAMExtTransport::SetBump, IAMExtTransportSetBump, SetBump, SetBump method [DirectShow], SetBump method [DirectShow],IAMExtTransport interface, dshow.iamexttransport_setbump, strmif/IAMExtTransport::SetBump
f1_keywords:
- strmif/IAMExtTransport.SetBump
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IAMExtTransport.SetBump
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMExtTransport::SetBump


## -description



The <code>SetBump</code> method temporarily changes the playback, for synchronization of multiple external devices.



This method is not implemented.


## -parameters




### -param Speed [in]

Specifies the temporary speed (a multiple of normal speed) as a <b>long</b> integer.


### -param Duration [in]

Specifies the duration of a bump as a <b>long</b> integer. The duration is given in the current time format; see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-settransportbasicparameters">IAMExtTransport::SetTransportBasicParameters</a> for more information.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



This method causes a temporary speed variation of the transport. The transport operates at the new speed until the specified duration elapses. Then it returns to its previous speed.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="https://docs.microsoft.com/windows/desktop/DirectShow/msdv-driver">MSDV</a> does not support this method. It returns E_NOTIMPL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-getbump">IAMExtTransport::GetBump</a>
 

 

