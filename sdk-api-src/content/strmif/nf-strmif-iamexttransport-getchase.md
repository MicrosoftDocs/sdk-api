---
UID: NF:strmif.IAMExtTransport.GetChase
title: IAMExtTransport::GetChase (strmif.h)
description: The GetChase method retrieves the status of chase mode.
helpviewer_keywords: ["GetChase","GetChase method [DirectShow]","GetChase method [DirectShow]","IAMExtTransport interface","IAMExtTransport interface [DirectShow]","GetChase method","IAMExtTransport.GetChase","IAMExtTransport::GetChase","IAMExtTransportGetChase","dshow.iamexttransport_getchase","strmif/IAMExtTransport::GetChase"]
old-location: dshow\iamexttransport_getchase.htm
tech.root: dshow
ms.assetid: 9ef12fa0-2ec9-45e5-9c22-20f810dac73b
ms.date: 12/05/2018
ms.keywords: GetChase, GetChase method [DirectShow], GetChase method [DirectShow],IAMExtTransport interface, IAMExtTransport interface [DirectShow],GetChase method, IAMExtTransport.GetChase, IAMExtTransport::GetChase, IAMExtTransportGetChase, dshow.iamexttransport_getchase, strmif/IAMExtTransport::GetChase
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
 - IAMExtTransport::GetChase
 - strmif/IAMExtTransport::GetChase
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
 - IAMExtTransport.GetChase
---

# IAMExtTransport::GetChase


## -description

The <code>GetChase</code> method retrieves the status of chase mode.



This method is not implemented.

## -parameters

### -param pEnabled [out]

Pointer to a <b>long</b> integer that receives one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OATRUE</td>
<td>Chase enabled.</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Chase disabled.</td>
</tr>
</table>

### -param pOffset [out]

Pointer to a <b>long</b> integer that receives an offset from the present time, indicating the offset that the transport will maintain while playing. The offset is given in the current time format; see <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-settransportbasicparameters">IAMExtTransport::SetTransportBasicParameters</a> for more information.

### -param phEvent [out]

Pointer to a variable that receives an event handle. The event is signaled when the chase offset is established.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-setchase">IAMExtTransport::SetChase</a>