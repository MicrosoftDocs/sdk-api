---
UID: NF:msctf.ITfThreadMgr.GetFunctionProvider
title: ITfThreadMgr::GetFunctionProvider (msctf.h)
description: ITfThreadMgr::GetFunctionProvider method
helpviewer_keywords: ["GUID_APP_FUNCTIONPROVIDER","GUID_SYSTEM_FUNCTIONPROVIDER","GetFunctionProvider","GetFunctionProvider method [Text Services Framework]","GetFunctionProvider method [Text Services Framework]","ITfThreadMgr interface","ITfThreadMgr interface [Text Services Framework]","GetFunctionProvider method","ITfThreadMgr.GetFunctionProvider","ITfThreadMgr::GetFunctionProvider","_tsf_itfthreadmgr_getfunctionprovider_ref","msctf/ITfThreadMgr::GetFunctionProvider","tsf.itfthreadmgr_getfunctionprovider"]
old-location: tsf\itfthreadmgr_getfunctionprovider.htm
tech.root: TSF
ms.assetid: b320790a-4b54-4475-97e6-e59f083cfc09
ms.date: 12/05/2018
ms.keywords: GUID_APP_FUNCTIONPROVIDER, GUID_SYSTEM_FUNCTIONPROVIDER, GetFunctionProvider, GetFunctionProvider method [Text Services Framework], GetFunctionProvider method [Text Services Framework],ITfThreadMgr interface, ITfThreadMgr interface [Text Services Framework],GetFunctionProvider method, ITfThreadMgr.GetFunctionProvider, ITfThreadMgr::GetFunctionProvider, _tsf_itfthreadmgr_getfunctionprovider_ref, msctf/ITfThreadMgr::GetFunctionProvider, tsf.itfthreadmgr_getfunctionprovider
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITfThreadMgr::GetFunctionProvider
 - msctf/ITfThreadMgr::GetFunctionProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfThreadMgr.GetFunctionProvider
---

# ITfThreadMgr::GetFunctionProvider


## -description

Obtains the specified function provider object.

## -parameters

### -param clsid [in]

CLSID of the desired function provider. This can be the CLSID of a function provider registered for the calling thread or one of the following predefined values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GUID_SYSTEM_FUNCTIONPROVIDER"></a><a id="guid_system_functionprovider"></a><dl>
<dt><b>GUID_SYSTEM_FUNCTIONPROVIDER</b></dt>
</dl>
</td>
<td width="60%">
Obtains the TSF system function provider.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_APP_FUNCTIONPROVIDER"></a><a id="guid_app_functionprovider"></a><dl>
<dt><b>GUID_APP_FUNCTIONPROVIDER</b></dt>
</dl>
</td>
<td width="60%">
Obtains the function provider implemented by the current application. This object is not available if the application does not register itself as a function provider.

</td>
</tr>
</table>

### -param ppFuncProv [out]

Pointer to a <a href="/windows/desktop/api/msctf/nn-msctf-itffunctionprovider">ITfFunctionProvider</a> interface that receives the function provider.

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
<dt><b>TF_E_NOPROVIDER</b></dt>
</dl>
</td>
<td width="60%">
No function provider matching <i>clsid</i> was available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
GUID_SYSTEM_FUNCTIONPROVIDER was requested, but cannot be obtained.

</td>
</tr>
</table>

## -remarks

A function provider registers by calling the TSF manager <a href="/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">ITfSourceSingle::AdviseSingleSink</a> method with IID_ITfFunctionProvider.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itffunctionprovider">ITfFunctionProvider
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">ITfSourceSingle::AdviseSingleSink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-enumfunctionproviders">ITfThreadMgr::EnumFunctionProviders
      </a>