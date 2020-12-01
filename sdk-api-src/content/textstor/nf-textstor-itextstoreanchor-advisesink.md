---
UID: NF:textstor.ITextStoreAnchor.AdviseSink
title: ITextStoreAnchor::AdviseSink (textstor.h)
description: The ITextStoreAnchor::AdviseSink method installs a new advise sink from the ITextStoreAnchorSink interface or modifies an existing advise sink.
helpviewer_keywords: ["AdviseSink","AdviseSink method [Text Services Framework]","AdviseSink method [Text Services Framework]","ITextStoreAnchor interface","ITextStoreAnchor interface [Text Services Framework]","AdviseSink method","ITextStoreAnchor.AdviseSink","ITextStoreAnchor::AdviseSink","textstor/ITextStoreAnchor::AdviseSink","tsf.itextstoreanchor_advisesink"]
old-location: tsf\itextstoreanchor_advisesink.htm
tech.root: TSF
ms.assetid: a2196d1c-b03e-44b4-b695-970feddb8ce5
ms.date: 12/05/2018
ms.keywords: AdviseSink, AdviseSink method [Text Services Framework], AdviseSink method [Text Services Framework],ITextStoreAnchor interface, ITextStoreAnchor interface [Text Services Framework],AdviseSink method, ITextStoreAnchor.AdviseSink, ITextStoreAnchor::AdviseSink, textstor/ITextStoreAnchor::AdviseSink, tsf.itextstoreanchor_advisesink
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITextStoreAnchor::AdviseSink
 - textstor/ITextStoreAnchor::AdviseSink
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
 - ITextStoreAnchor.AdviseSink
---

# ITextStoreAnchor::AdviseSink


## -description

The <b>ITextStoreAnchor::AdviseSink</b> method installs a new advise sink from the <a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchorsink">ITextStoreAnchorSink</a> interface or modifies an existing advise sink.

## -parameters

### -param riid [in]

Specifies the sink interface. The only supported value is IID_ITextStoreAnchorSink.

### -param punk [in]

Pointer to the sink interface to advise. Cannot be <b>NULL</b>.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The specified sink interface <i>riid</i> could not be obtained.

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

## -remarks

Subsequent calls with the same interface, represented by the <i>punk</i> parameter, are handled as requests to update the <i>dwMask</i> parameter. Servers should not call the <b>AddRef</b> method on the sink in response to such a request.

Servers only maintain a single connection point. Attempts to advise a second sink object fail until the original sink object is removed. Applications should use the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-unadvisesink">ITextStoreAnchor::UnadviseSink</a> method to unregister the sink object when notifications are not required.

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-unadvisesink">ITextStoreAnchor::UnadviseSink
      </a>



<a href="/windows/desktop/TSF/ts-as--constants">TS_AS_* Constants
      </a>