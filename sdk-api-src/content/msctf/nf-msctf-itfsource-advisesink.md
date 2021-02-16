---
UID: NF:msctf.ITfSource.AdviseSink
title: ITfSource::AdviseSink (msctf.h)
description: ITfSource::AdviseSink method
helpviewer_keywords: ["AdviseSink","AdviseSink method [Text Services Framework]","AdviseSink method [Text Services Framework]","ITfSource interface","IID_ITfActiveLanguageProfileNotifySink","IID_ITfDisplayAttributeNotifySink","IID_ITfKeyTraceEventSink","IID_ITfPreservedKeyNotifySink","IID_ITfThreadFocusSink","IID_ITfThreadMgrEventSink","ITfSource interface [Text Services Framework]","AdviseSink method","ITfSource.AdviseSink","ITfSource::AdviseSink","_tsf_itfsource_advisesink_ref","msctf/ITfSource::AdviseSink","tsf.itfsource_advisesink"]
old-location: tsf\itfsource_advisesink.htm
tech.root: TSF
ms.assetid: 90928e6e-e11e-42ad-9b3e-d974642aca36
ms.date: 12/05/2018
ms.keywords: AdviseSink, AdviseSink method [Text Services Framework], AdviseSink method [Text Services Framework],ITfSource interface, IID_ITfActiveLanguageProfileNotifySink, IID_ITfDisplayAttributeNotifySink, IID_ITfKeyTraceEventSink, IID_ITfPreservedKeyNotifySink, IID_ITfThreadFocusSink, IID_ITfThreadMgrEventSink, ITfSource interface [Text Services Framework],AdviseSink method, ITfSource.AdviseSink, ITfSource::AdviseSink, _tsf_itfsource_advisesink_ref, msctf/ITfSource::AdviseSink, tsf.itfsource_advisesink
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
 - ITfSource::AdviseSink
 - msctf/ITfSource::AdviseSink
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
 - ITfSource.AdviseSink
---

# ITfSource::AdviseSink


## -description

Installs an advise sink.

## -parameters

### -param riid [in]

Identifies the type of advise sink to install.

This parameter can be one of the following values when the <b>ITfSource</b> object is obtained from an <a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr</a> object.

This parameter can be one of the following values when the <a href="/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a> object is obtained from an <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> object.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IID_ITfActiveLanguageProfileNotifySink"></a><a id="iid_itfactivelanguageprofilenotifysink"></a><a id="IID_ITFACTIVELANGUAGEPROFILENOTIFYSINK"></a><dl>
<dt><b>IID_ITfActiveLanguageProfileNotifySink</b></dt>
</dl>
</td>
<td width="60%">
Installs an <a href="/windows/desktop/api/msctf/nn-msctf-itfactivelanguageprofilenotifysink">ITfActiveLanguageProfileNotifySink</a> advise sink.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_ITfDisplayAttributeNotifySink"></a><a id="iid_itfdisplayattributenotifysink"></a><a id="IID_ITFDISPLAYATTRIBUTENOTIFYSINK"></a><dl>
<dt><b>IID_ITfDisplayAttributeNotifySink</b></dt>
</dl>
</td>
<td width="60%">
Installs an <a href="/windows/desktop/api/msctf/nn-msctf-itfdisplayattributenotifysink">ITfDisplayAttributeNotifySink</a> advise sink.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_ITfKeyTraceEventSink"></a><a id="iid_itfkeytraceeventsink"></a><a id="IID_ITFKEYTRACEEVENTSINK"></a><dl>
<dt><b>IID_ITfKeyTraceEventSink</b></dt>
</dl>
</td>
<td width="60%">
Installs an <a href="/windows/desktop/api/msctf/nn-msctf-itfkeytraceeventsink">ITfKeyTraceEventSink</a> advise sink.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_ITfPreservedKeyNotifySink"></a><a id="iid_itfpreservedkeynotifysink"></a><a id="IID_ITFPRESERVEDKEYNOTIFYSINK"></a><dl>
<dt><b>IID_ITfPreservedKeyNotifySink</b></dt>
</dl>
</td>
<td width="60%">
Installs an <a href="/windows/desktop/api/msctf/nn-msctf-itfpreservedkeynotifysink">ITfPreservedKeyNotifySink</a> advise sink.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_ITfThreadFocusSink"></a><a id="iid_itfthreadfocussink"></a><a id="IID_ITFTHREADFOCUSSINK"></a><dl>
<dt><b>IID_ITfThreadFocusSink</b></dt>
</dl>
</td>
<td width="60%">
Installs an <a href="/windows/desktop/api/msctf/nn-msctf-itfthreadfocussink">ITfThreadFocusSink</a> advise sink.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_ITfThreadMgrEventSink"></a><a id="iid_itfthreadmgreventsink"></a><a id="IID_ITFTHREADMGREVENTSINK"></a><dl>
<dt><b>IID_ITfThreadMgrEventSink</b></dt>
</dl>
</td>
<td width="60%">
Installs an <a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgreventsink">ITfThreadMgrEventSink</a> advise sink.

</td>
</tr>
</table>

### -param punk [in]

The advise sink <b>IUnknown</b> pointer.

### -param pdwCookie [out]

Address of a DWORD value that receives an identifying cookie. This value is used to uninstall the advise sink in a subsequent call to <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink">ITfSource::UnadviseSink</a>. Receives (DWORD)-1 if a failure occurs.

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

<a href="/windows/desktop/api/msctf/nn-msctf-itfactivelanguageprofilenotifysink">ITfActiveLanguageProfileNotifySink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcompartment">ITfCompartment
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcompartmenteventsink">ITfCompartmentEventSink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontextkeyeventsink">ITfContextKeyEventSink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfdisplayattributenotifysink">ITfDisplayAttributeNotifySink
      </a>



ITfEditTransactionSink



<a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfkeytraceeventsink">ITfKeyTraceEventSink
      </a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem
      </a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemsink">ITfLangBarItemSink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itflanguageprofilenotifysink">ITfLanguageProfileNotifySink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfpreservedkeynotifysink">ITfPreservedKeyNotifySink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink">ITfSource::UnadviseSink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfstatussink">ITfStatusSink
      </a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritemsink">ITfSystemLangBarItemSink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itftexteditsink">ITfTextEditSink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itftextlayoutsink">ITfTextLayoutSink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadfocussink">ITfThreadFocusSink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgreventsink">ITfThreadMgrEventSink
      </a>