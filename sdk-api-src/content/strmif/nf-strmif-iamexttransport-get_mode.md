---
UID: NF:strmif.IAMExtTransport.get_Mode
title: IAMExtTransport::get_Mode (strmif.h)
description: The get_Mode method retrieves the current transport mode, such as play, stop, or record.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","get_Mode method","IAMExtTransport.get_Mode","IAMExtTransport::get_Mode","IAMExtTransportget_Mode","dshow.iamexttransport_get_mode","get_Mode","get_Mode method [DirectShow]","get_Mode method [DirectShow]","IAMExtTransport interface","strmif/IAMExtTransport::get_Mode"]
old-location: dshow\iamexttransport_get_mode.htm
tech.root: dshow
ms.assetid: ee08cca0-a2ea-4a7c-8714-f22d5cd62fe8
ms.date: 12/05/2018
ms.keywords: IAMExtTransport interface [DirectShow],get_Mode method, IAMExtTransport.get_Mode, IAMExtTransport::get_Mode, IAMExtTransportget_Mode, dshow.iamexttransport_get_mode, get_Mode, get_Mode method [DirectShow], get_Mode method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::get_Mode
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
 - IAMExtTransport::get_Mode
 - strmif/IAMExtTransport::get_Mode
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
 - IAMExtTransport.get_Mode
---

# IAMExtTransport::get_Mode


## -description

The <code>get_Mode</code> method retrieves the current transport mode, such as play, stop, or record.

## -parameters

### -param pMode [out]

Pointer to a <b>long</b> integer that receives the current transport mode. For possible values, see <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-put_mode">IAMExtTransport::put_Mode</a>.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>