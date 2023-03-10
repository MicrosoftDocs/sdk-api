---
UID: NF:msctf.ITfSourceSingle.AdviseSingleSink
title: ITfSourceSingle::AdviseSingleSink (msctf.h)
description: ITfSourceSingle::AdviseSingleSink method
helpviewer_keywords: ["AdviseSingleSink","AdviseSingleSink method [Text Services Framework]","AdviseSingleSink method [Text Services Framework]","ITfSourceSingle interface","IID_ITfCleanupContextDurationSink","IID_ITfFunctionProvider","ITfSourceSingle interface [Text Services Framework]","AdviseSingleSink method","ITfSourceSingle.AdviseSingleSink","ITfSourceSingle::AdviseSingleSink","_tsf_itfsourcesingle_advisesinglesink_ref","msctf/ITfSourceSingle::AdviseSingleSink","tsf.itfsourcesingle_advisesinglesink"]
old-location: tsf\itfsourcesingle_advisesinglesink.htm
tech.root: TSF
ms.assetid: d9231f36-24c4-4d46-97e7-518f5fcc1ce2
ms.date: 12/05/2018
ms.keywords: AdviseSingleSink, AdviseSingleSink method [Text Services Framework], AdviseSingleSink method [Text Services Framework],ITfSourceSingle interface, IID_ITfCleanupContextDurationSink, IID_ITfFunctionProvider, ITfSourceSingle interface [Text Services Framework],AdviseSingleSink method, ITfSourceSingle.AdviseSingleSink, ITfSourceSingle::AdviseSingleSink, _tsf_itfsourcesingle_advisesinglesink_ref, msctf/ITfSourceSingle::AdviseSingleSink, tsf.itfsourcesingle_advisesinglesink
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
 - ITfSourceSingle::AdviseSingleSink
 - msctf/ITfSourceSingle::AdviseSingleSink
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
 - ITfSourceSingle.AdviseSingleSink
---

# ITfSourceSingle::AdviseSingleSink


## -description

Installs an advise sink.

## -parameters

### -param tid [in]

Contains a <b>TfClientId</b> value that identifies the client.

### -param riid [in]

Identifies the type of advise sink to install.

This parameter can be one of the following values when the <a href="/windows/desktop/api/msctf/nn-msctf-itfsourcesingle">ITfSourceSingle</a> object is obtained from an <a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr</a> object.

This parameter can be one of the following values when the <b>ITfSourceSingle</b> object is obtained from an <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> object.

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
Installs a <a href="/windows/desktop/api/msctf/nn-msctf-itfcleanupcontextdurationsink">ITfCleanupContextDurationSink</a> advise sink.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_ITfFunctionProvider"></a><a id="iid_itffunctionprovider"></a><a id="IID_ITFFUNCTIONPROVIDER"></a><dl>
<dt><b>IID_ITfFunctionProvider</b></dt>
</dl>
</td>
<td width="60%">
Registers the client as a function provider. The <i>punk</i> parameter is an <a href="/windows/desktop/api/msctf/nn-msctf-itffunctionprovider">ITfFunctionProvider</a> interface pointer.

</td>
</tr>
</table>

### -param punk [in]

Pointer to the advise sink <b>IUnknown</b> pointer.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_CANNOTCONNECT</b></dt>
</dl>
</td>
<td width="60%">
The advise sink cannot be installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_ADVISELIMIT</b></dt>
</dl>
</td>
<td width="60%">
The maximum number of advise sinks has been reached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcleanupcontextsink">ITfCleanupContextSink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itffunctionprovider">ITfFunctionProvider
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfsourcesingle">ITfSourceSingle</a>