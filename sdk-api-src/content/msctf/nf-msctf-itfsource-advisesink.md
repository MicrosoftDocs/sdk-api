---
UID: NF:msctf.ITfSource.AdviseSink
title: ITfSource::AdviseSink
author: windows-sdk-content
description: ITfSource::AdviseSink method
old-location: tsf\itfsource_advisesink.htm
old-project: TSF
ms.assetid: 90928e6e-e11e-42ad-9b3e-d974642aca36
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AdviseSink, AdviseSink method [Text Services Framework], AdviseSink method [Text Services Framework],ITfSource interface, IID_ITfActiveLanguageProfileNotifySink, IID_ITfDisplayAttributeNotifySink, IID_ITfKeyTraceEventSink, IID_ITfPreservedKeyNotifySink, IID_ITfThreadFocusSink, IID_ITfThreadMgrEventSink, ITfSource interface [Text Services Framework],AdviseSink method, ITfSource.AdviseSink, ITfSource::AdviseSink, _tsf_itfsource_advisesink_ref, msctf/ITfSource::AdviseSink, tsf.itfsource_advisesink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfSource.AdviseSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfSource::AdviseSink


## -description




## -parameters




### -param riid [in]

Identifies the type of advise sink to install.

This parameter can be one of the following values when the <b>ITfSource</b> object is obtained from an <a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a> object.

This parameter can be one of the following values when the <a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">ITfSource</a> object is obtained from an <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> object.

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
Installs an <a href="https://msdn.microsoft.com/c70141e8-c948-44f4-914e-454327aadf2b">ITfActiveLanguageProfileNotifySink</a> advise sink.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_ITfDisplayAttributeNotifySink"></a><a id="iid_itfdisplayattributenotifysink"></a><a id="IID_ITFDISPLAYATTRIBUTENOTIFYSINK"></a><dl>
<dt><b>IID_ITfDisplayAttributeNotifySink</b></dt>
</dl>
</td>
<td width="60%">
Installs an <a href="https://msdn.microsoft.com/c21ff404-af42-488a-90f0-d3f02277c557">ITfDisplayAttributeNotifySink</a> advise sink.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_ITfKeyTraceEventSink"></a><a id="iid_itfkeytraceeventsink"></a><a id="IID_ITFKEYTRACEEVENTSINK"></a><dl>
<dt><b>IID_ITfKeyTraceEventSink</b></dt>
</dl>
</td>
<td width="60%">
Installs an <a href="https://msdn.microsoft.com/29785bae-59b8-4bbb-b899-44f6fc3e83bd">ITfKeyTraceEventSink</a> advise sink.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_ITfPreservedKeyNotifySink"></a><a id="iid_itfpreservedkeynotifysink"></a><a id="IID_ITFPRESERVEDKEYNOTIFYSINK"></a><dl>
<dt><b>IID_ITfPreservedKeyNotifySink</b></dt>
</dl>
</td>
<td width="60%">
Installs an <a href="https://msdn.microsoft.com/0bf786b5-efcd-4c58-835b-47e7adf9be63">ITfPreservedKeyNotifySink</a> advise sink.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_ITfThreadFocusSink"></a><a id="iid_itfthreadfocussink"></a><a id="IID_ITFTHREADFOCUSSINK"></a><dl>
<dt><b>IID_ITfThreadFocusSink</b></dt>
</dl>
</td>
<td width="60%">
Installs an <a href="https://msdn.microsoft.com/17335fa9-01ee-4585-9454-f326b6281ab1">ITfThreadFocusSink</a> advise sink.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_ITfThreadMgrEventSink"></a><a id="iid_itfthreadmgreventsink"></a><a id="IID_ITFTHREADMGREVENTSINK"></a><dl>
<dt><b>IID_ITfThreadMgrEventSink</b></dt>
</dl>
</td>
<td width="60%">
Installs an <a href="https://msdn.microsoft.com/be2a3eb1-cb17-4d8b-a44d-ccb33749c8f6">ITfThreadMgrEventSink</a> advise sink.

</td>
</tr>
</table>
 


### -param punk [in]

The advise sink <b>IUnknown</b> pointer.


### -param pdwCookie [out]

Address of a DWORD value that receives an identifying cookie. This value is used to uninstall the advise sink in a subsequent call to <a href="https://msdn.microsoft.com/e5d40c6f-c8ab-4e53-94d0-a6b475ce7a84">ITfSource::UnadviseSink</a>. Receives (DWORD)-1 if a failure occurs.


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




<a href="https://msdn.microsoft.com/c70141e8-c948-44f4-914e-454327aadf2b">ITfActiveLanguageProfileNotifySink
      </a>



<a href="https://msdn.microsoft.com/c9ca3eb5-1fb1-4e45-9ec4-a0296f1bc8c3">ITfCompartment
      </a>



<a href="https://msdn.microsoft.com/1bd464e7-9e34-4725-83f9-42e09ddf4778">ITfCompartmentEventSink
      </a>



<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/26fc5d8a-e24e-414e-a355-c1f89251f6bd">ITfContextKeyEventSink
      </a>



<a href="https://msdn.microsoft.com/c21ff404-af42-488a-90f0-d3f02277c557">ITfDisplayAttributeNotifySink
      </a>



ITfEditTransactionSink



<a href="https://msdn.microsoft.com/9fa722a4-1e3f-4845-aea7-3b24b517f2a5">ITfInputProcessorProfiles
      </a>



<a href="https://msdn.microsoft.com/29785bae-59b8-4bbb-b899-44f6fc3e83bd">ITfKeyTraceEventSink
      </a>



<a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">ITfLangBarItem
      </a>



<a href="https://msdn.microsoft.com/1734a011-1ee8-4afd-ace8-334eeaf14518">ITfLangBarItemSink
      </a>



<a href="https://msdn.microsoft.com/c0c8d02a-cc3f-4c1c-96e9-516f49b868e6">ITfLanguageProfileNotifySink
      </a>



<a href="https://msdn.microsoft.com/0bf786b5-efcd-4c58-835b-47e7adf9be63">ITfPreservedKeyNotifySink
      </a>



<a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">ITfSource</a>



<a href="https://msdn.microsoft.com/e5d40c6f-c8ab-4e53-94d0-a6b475ce7a84">ITfSource::UnadviseSink
      </a>



<a href="https://msdn.microsoft.com/5fc37251-938b-4581-bb54-816749b17001">ITfStatusSink
      </a>



<a href="https://msdn.microsoft.com/a88b20ec-fc54-4814-9ca1-131664b4f377">ITfSystemLangBarItemSink
      </a>



<a href="https://msdn.microsoft.com/50f44525-eb3a-4db2-90c2-3e0c6c6146e3">ITfTextEditSink
      </a>



<a href="https://msdn.microsoft.com/370e30a8-6eed-448a-87c7-7fd01e9973c6">ITfTextLayoutSink
      </a>



<a href="https://msdn.microsoft.com/17335fa9-01ee-4585-9454-f326b6281ab1">ITfThreadFocusSink
      </a>



<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr
      </a>



<a href="https://msdn.microsoft.com/be2a3eb1-cb17-4d8b-a44d-ccb33749c8f6">ITfThreadMgrEventSink
      </a>
 

 

