---
UID: NF:strmif.IAMExtTransport.get_AntiClogControl
title: IAMExtTransport::get_AntiClogControl (strmif.h)
description: The get_AntiClogControl method determines whether the anti-headclog control is enabled or disabled.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","get_AntiClogControl method","IAMExtTransport.get_AntiClogControl","IAMExtTransport::get_AntiClogControl","IAMExtTransportget_AntiClogControl","dshow.iamexttransport_get_anticlogcontrol","get_AntiClogControl","get_AntiClogControl method [DirectShow]","get_AntiClogControl method [DirectShow]","IAMExtTransport interface","strmif/IAMExtTransport::get_AntiClogControl"]
old-location: dshow\iamexttransport_get_anticlogcontrol.htm
tech.root: dshow
ms.assetid: e0175b44-d1e6-4f3a-8aa7-893b41d0c487
ms.date: 12/05/2018
ms.keywords: IAMExtTransport interface [DirectShow],get_AntiClogControl method, IAMExtTransport.get_AntiClogControl, IAMExtTransport::get_AntiClogControl, IAMExtTransportget_AntiClogControl, dshow.iamexttransport_get_anticlogcontrol, get_AntiClogControl, get_AntiClogControl method [DirectShow], get_AntiClogControl method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::get_AntiClogControl
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
 - IAMExtTransport::get_AntiClogControl
 - strmif/IAMExtTransport::get_AntiClogControl
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
 - IAMExtTransport.get_AntiClogControl
---

# IAMExtTransport::get_AntiClogControl


## -description

The <code>get_AntiClogControl</code> method determines whether the anti-headclog control is enabled or disabled.



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
<td>Anti-headclog is enabled.</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Anti-headclog is disabled.</td>
</tr>
</table>

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-put_anticlogcontrol">IAMExtTransport::put_AntiClogControl</a>