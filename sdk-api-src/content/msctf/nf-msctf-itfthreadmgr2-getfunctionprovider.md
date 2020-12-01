---
UID: NF:msctf.ITfThreadMgr2.GetFunctionProvider
title: ITfThreadMgr2::GetFunctionProvider (msctf.h)
description: Obtains the specified function provider object.
helpviewer_keywords: ["GUID_APP_FUNCTIONPROVIDER","GUID_SYSTEM_FUNCTIONPROVIDER","GetFunctionProvider","GetFunctionProvider method [Text Services Framework]","GetFunctionProvider method [Text Services Framework]","ITfThreadMgr2 interface","ITfThreadMgr2 interface [Text Services Framework]","GetFunctionProvider method","ITfThreadMgr2.GetFunctionProvider","ITfThreadMgr2::GetFunctionProvider","msctf/ITfThreadMgr2::GetFunctionProvider","tsf.itfthreadmgr2_getfunctionprovider"]
old-location: tsf\itfthreadmgr2_getfunctionprovider.htm
tech.root: TSF
ms.assetid: 4B2B2098-ECA1-454F-8F7F-978893C466F7
ms.date: 12/05/2018
ms.keywords: GUID_APP_FUNCTIONPROVIDER, GUID_SYSTEM_FUNCTIONPROVIDER, GetFunctionProvider, GetFunctionProvider method [Text Services Framework], GetFunctionProvider method [Text Services Framework],ITfThreadMgr2 interface, ITfThreadMgr2 interface [Text Services Framework],GetFunctionProvider method, ITfThreadMgr2.GetFunctionProvider, ITfThreadMgr2::GetFunctionProvider, msctf/ITfThreadMgr2::GetFunctionProvider, tsf.itfthreadmgr2_getfunctionprovider
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfThreadMgr2::GetFunctionProvider
 - msctf/ITfThreadMgr2::GetFunctionProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.h
api_name:
 - ITfThreadMgr2.GetFunctionProvider
---

# ITfThreadMgr2::GetFunctionProvider


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

<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr2">ITfThreadMgr2</a>