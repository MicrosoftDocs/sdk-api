---
UID: NF:textstor.ITextStoreACP2.AdviseSink
title: ITextStoreACP2::AdviseSink (textstor.h)
description: Installs a new advise sink from the ITextStoreACPSink interface or modifies an existing advise sink. The sink interface is specified by the punk parameter.
helpviewer_keywords: ["AdviseSink","AdviseSink method [Text Services Framework]","AdviseSink method [Text Services Framework]","ITextStoreACP2 interface","ITextStoreACP2 interface [Text Services Framework]","AdviseSink method","ITextStoreACP2.AdviseSink","ITextStoreACP2::AdviseSink","textstor/ITextStoreACP2::AdviseSink","tsf.itextstoreacp2_advisesink"]
old-location: tsf\itextstoreacp2_advisesink.htm
tech.root: TSF
ms.assetid: 15fa2f85-3fe8-4e2d-bd3b-a270182adc66
ms.date: 12/05/2018
ms.keywords: AdviseSink, AdviseSink method [Text Services Framework], AdviseSink method [Text Services Framework],ITextStoreACP2 interface, ITextStoreACP2 interface [Text Services Framework],AdviseSink method, ITextStoreACP2.AdviseSink, ITextStoreACP2::AdviseSink, textstor/ITextStoreACP2::AdviseSink, tsf.itextstoreacp2_advisesink
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStoreACP2::AdviseSink
 - textstor/ITextStoreACP2::AdviseSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACP2.AdviseSink
---

# ITextStoreACP2::AdviseSink


## -description

Installs a new advise sink from the <a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacpsink">ITextStoreACPSink</a> interface or modifies an existing advise sink. The sink interface is specified by the <i>punk</i> parameter.

## -parameters

### -param riid [in]

Specifies the sink interface.

### -param punk [in]

Pointer to the sink interface. Cannot be <b>NULL</b>.

### -param dwMask [in]

Specifies the events that notify the advise sink. For more information about possible parameter values, see <a href="/windows/desktop/TSF/ts-as--constants">TS_AS_* Constants</a>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_ADVISELIMIT</b></dt>
</dl>
</td>
<td width="60%">
A sink interface pointer could not be obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified sink interface is unsupported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The specified sink object could not be obtained.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>