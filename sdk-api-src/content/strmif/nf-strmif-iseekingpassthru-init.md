---
UID: NF:strmif.ISeekingPassThru.Init
title: ISeekingPassThru::Init (strmif.h)
description: The Init method initializes the seeking helper object.
helpviewer_keywords: ["ISeekingPassThru interface [DirectShow]","Init method","ISeekingPassThru.Init","ISeekingPassThru::Init","ISeekingPassThruInit","Init","Init method [DirectShow]","Init method [DirectShow]","ISeekingPassThru interface","dshow.iseekingpassthru_init","strmif/ISeekingPassThru::Init"]
old-location: dshow\iseekingpassthru_init.htm
tech.root: dshow
ms.assetid: bb32c20c-bbae-403a-885b-f07c6dcf46f4
ms.date: 12/05/2018
ms.keywords: ISeekingPassThru interface [DirectShow],Init method, ISeekingPassThru.Init, ISeekingPassThru::Init, ISeekingPassThruInit, Init, Init method [DirectShow], Init method [DirectShow],ISeekingPassThru interface, dshow.iseekingpassthru_init, strmif/ISeekingPassThru::Init
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
 - ISeekingPassThru::Init
 - strmif/ISeekingPassThru::Init
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
 - ISeekingPassThru.Init
---

# ISeekingPassThru::Init


## -description

The <code>Init</code> method initializes the seeking helper object.

## -parameters

### -param bSupportRendering [in]

Boolean value that specifies whether the filter is a renderer. Use the value <b>TRUE</b> if the filter is a renderer, or <b>FALSE</b> otherwise.

### -param pPin [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface on the input pin of the filter.

## -returns

Returns one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Object was already initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to create the object.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iseekingpassthru">ISeekingPassThru Interface</a>