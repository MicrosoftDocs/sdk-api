---
UID: NF:msctf.ITfSourceSingle.UnadviseSingleSink
title: ITfSourceSingle::UnadviseSingleSink (msctf.h)
description: ITfSourceSingle::UnadviseSingleSink method
helpviewer_keywords: ["IID_ITfCleanupContextDurationSink","IID_ITfCleanupContextSink","IID_ITfFunctionProvider","ITfSourceSingle interface [Text Services Framework]","UnadviseSingleSink method","ITfSourceSingle.UnadviseSingleSink","ITfSourceSingle::UnadviseSingleSink","UnadviseSingleSink","UnadviseSingleSink method [Text Services Framework]","UnadviseSingleSink method [Text Services Framework]","ITfSourceSingle interface","_tsf_itfsourcesingle_unadvisesinglesink_ref","msctf/ITfSourceSingle::UnadviseSingleSink","tsf.itfsourcesingle_unadvisesinglesink"]
old-location: tsf\itfsourcesingle_unadvisesinglesink.htm
tech.root: TSF
ms.assetid: 1689dedb-c168-4a05-b598-517c87d9afbd
ms.date: 12/05/2018
ms.keywords: IID_ITfCleanupContextDurationSink, IID_ITfCleanupContextSink, IID_ITfFunctionProvider, ITfSourceSingle interface [Text Services Framework],UnadviseSingleSink method, ITfSourceSingle.UnadviseSingleSink, ITfSourceSingle::UnadviseSingleSink, UnadviseSingleSink, UnadviseSingleSink method [Text Services Framework], UnadviseSingleSink method [Text Services Framework],ITfSourceSingle interface, _tsf_itfsourcesingle_unadvisesinglesink_ref, msctf/ITfSourceSingle::UnadviseSingleSink, tsf.itfsourcesingle_unadvisesinglesink
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - ITfSourceSingle::UnadviseSingleSink
 - msctf/ITfSourceSingle::UnadviseSingleSink
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
 - ITfSourceSingle.UnadviseSingleSink
---

# ITfSourceSingle::UnadviseSingleSink


## -description

Uninstalls an advise sink.

## -parameters

### -param tid [in]

Contains a <b>TfClientId</b> value that identifies the client.

### -param riid [in]

Identifies the type of advise sink to uninstall. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IID_ITfCleanupContextDurationSink"></a><a id="iid_itfcleanupcontextdurationsink"></a><a id="IID_ITFCLEANUPCONTEXTDURATIONSINK"></a><dl>
<dt><b>IID_ITfCleanupContextDurationSink</b></dt>
</dl>
</td>
<td width="60%">
Uninstalls the <a href="/windows/desktop/api/msctf/nn-msctf-itfcleanupcontextdurationsink">ITfCleanupContextDurationSink</a> advise sink. Applies to: Text service

</td>
</tr>
<tr>
<td width="40%"><a id="IID_ITfCleanupContextSink"></a><a id="iid_itfcleanupcontextsink"></a><a id="IID_ITFCLEANUPCONTEXTSINK"></a><dl>
<dt><b>IID_ITfCleanupContextSink</b></dt>
</dl>
</td>
<td width="60%">
Uninstalls the <a href="/windows/desktop/api/msctf/nn-msctf-itfcleanupcontextsink">ITfCleanupContextSink</a> advise sink. Applies to: Text service

</td>
</tr>
<tr>
<td width="40%"><a id="IID_ITfFunctionProvider"></a><a id="iid_itffunctionprovider"></a><a id="IID_ITFFUNCTIONPROVIDER"></a><dl>
<dt><b>IID_ITfFunctionProvider</b></dt>
</dl>
</td>
<td width="60%">
Unregisters the client as a function provider. Applies to: Text Service and Application

</td>
</tr>
</table>

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
The advise sink was successfully uninstalled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>tid</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The advise sink is not installed.

</td>
</tr>
</table>