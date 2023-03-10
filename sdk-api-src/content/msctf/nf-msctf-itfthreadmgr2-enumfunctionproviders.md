---
UID: NF:msctf.ITfThreadMgr2.EnumFunctionProviders
title: ITfThreadMgr2::EnumFunctionProviders (msctf.h)
description: Obtains an enumerator for all of the function providers registered for the calling thread.
helpviewer_keywords: ["EnumFunctionProviders","EnumFunctionProviders method [Text Services Framework]","EnumFunctionProviders method [Text Services Framework]","ITfThreadMgr2 interface","ITfThreadMgr2 interface [Text Services Framework]","EnumFunctionProviders method","ITfThreadMgr2.EnumFunctionProviders","ITfThreadMgr2::EnumFunctionProviders","msctf/ITfThreadMgr2::EnumFunctionProviders","tsf.itfthreadmgr2_enumfunctionproviders"]
old-location: tsf\itfthreadmgr2_enumfunctionproviders.htm
tech.root: TSF
ms.assetid: 0F28BDFD-4CD8-4D50-92D9-6A60B80122B2
ms.date: 12/05/2018
ms.keywords: EnumFunctionProviders, EnumFunctionProviders method [Text Services Framework], EnumFunctionProviders method [Text Services Framework],ITfThreadMgr2 interface, ITfThreadMgr2 interface [Text Services Framework],EnumFunctionProviders method, ITfThreadMgr2.EnumFunctionProviders, ITfThreadMgr2::EnumFunctionProviders, msctf/ITfThreadMgr2::EnumFunctionProviders, tsf.itfthreadmgr2_enumfunctionproviders
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
 - ITfThreadMgr2::EnumFunctionProviders
 - msctf/ITfThreadMgr2::EnumFunctionProviders
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
 - ITfThreadMgr2.EnumFunctionProviders
---

# ITfThreadMgr2::EnumFunctionProviders


## -description

Obtains an enumerator for all of the function providers registered for the calling thread.

## -parameters

### -param ppEnum [out]

Address of a <a href="/windows/desktop/api/msctf/nn-msctf-ienumtffunctionproviders">IEnumTfFunctionProviders</a> interface that receives the function provider enumerator.

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
<i>ppEnum</i> is invalid.

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
</table>

## -remarks

The enumerator only contains the registered function providers. The enumerator will not contain the predefined function providers as described in <a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-getfunctionprovider">GetFunctionProvider</a>.

A function provider registers itself by calling the TSF manager <a href="/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">ITfSourceSingle::AdviseSingleSink</a> method with IID_ITfFunctionProvider.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr2">ITfThreadMgr2</a>