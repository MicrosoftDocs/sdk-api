---
UID: NF:strmif.IAMExtTransport.get_EditStart
title: IAMExtTransport::get_EditStart (strmif.h)
description: The get_EditStart method determines whether the external transport's edit control is active.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","get_EditStart method","IAMExtTransport.get_EditStart","IAMExtTransport::get_EditStart","IAMExtTransportget_EditStart","dshow.iamexttransport_get_editstart","get_EditStart","get_EditStart method [DirectShow]","get_EditStart method [DirectShow]","IAMExtTransport interface","strmif/IAMExtTransport::get_EditStart"]
old-location: dshow\iamexttransport_get_editstart.htm
tech.root: dshow
ms.assetid: 83eb6f22-646c-400a-8adb-5545914656c9
ms.date: 12/05/2018
ms.keywords: IAMExtTransport interface [DirectShow],get_EditStart method, IAMExtTransport.get_EditStart, IAMExtTransport::get_EditStart, IAMExtTransportget_EditStart, dshow.iamexttransport_get_editstart, get_EditStart, get_EditStart method [DirectShow], get_EditStart method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::get_EditStart
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
 - IAMExtTransport::get_EditStart
 - strmif/IAMExtTransport::get_EditStart
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
 - IAMExtTransport.get_EditStart
---

# IAMExtTransport::get_EditStart


## -description

The <code>get_EditStart</code> method determines whether the external transport's edit control is active.



This method is not implemented.

## -parameters

### -param pValue [out]

Specifies a pointer to a <b>long</b> integer to receive a value indicating whether the external transport's edit control is active.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OATRUE</td>
<td>Edit control is active.</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Edit control is inactive.</td>
</tr>
</table>

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-put_editstart">IAMExtTransport::put_EditStart</a>