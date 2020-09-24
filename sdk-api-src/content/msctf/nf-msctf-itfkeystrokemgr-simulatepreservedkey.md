---
UID: NF:msctf.ITfKeystrokeMgr.SimulatePreservedKey
title: ITfKeystrokeMgr::SimulatePreservedKey (msctf.h)
description: ITfKeystrokeMgr::SimulatePreservedKey method
helpviewer_keywords: ["ITfKeystrokeMgr interface [Text Services Framework]","SimulatePreservedKey method","ITfKeystrokeMgr.SimulatePreservedKey","ITfKeystrokeMgr::SimulatePreservedKey","SimulatePreservedKey","SimulatePreservedKey method [Text Services Framework]","SimulatePreservedKey method [Text Services Framework]","ITfKeystrokeMgr interface","_tsf_itfkeystrokemgr_simulatepreservedkey_ref","msctf/ITfKeystrokeMgr::SimulatePreservedKey","tsf.itfkeystrokemgr_simulatepreservedkey"]
old-location: tsf\itfkeystrokemgr_simulatepreservedkey.htm
tech.root: TSF
ms.assetid: 09ad2203-a254-4afd-bdee-b8c51daa6e95
ms.date: 12/05/2018
ms.keywords: ITfKeystrokeMgr interface [Text Services Framework],SimulatePreservedKey method, ITfKeystrokeMgr.SimulatePreservedKey, ITfKeystrokeMgr::SimulatePreservedKey, SimulatePreservedKey, SimulatePreservedKey method [Text Services Framework], SimulatePreservedKey method [Text Services Framework],ITfKeystrokeMgr interface, _tsf_itfkeystrokemgr_simulatepreservedkey_ref, msctf/ITfKeystrokeMgr::SimulatePreservedKey, tsf.itfkeystrokemgr_simulatepreservedkey
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
 - ITfKeystrokeMgr::SimulatePreservedKey
 - msctf/ITfKeystrokeMgr::SimulatePreservedKey
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
 - ITfKeystrokeMgr.SimulatePreservedKey
---

# ITfKeystrokeMgr::SimulatePreservedKey


## -description

Simulates the execution of a preserved key sequence.

## -parameters

### -param pic [in]

Pointer to the application context. This value was returned by a previous call to <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a>.

### -param rguid [in]

Contains the command GUID of the preserved key.

### -param pfEaten [out]

Pointer to a BOOL that indicates if the key event was handled. If this value receives <b>TRUE</b>, the key event was handled. If this value is <b>FALSE</b>, the key event was not handled.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The preserved key cannot be simulated.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfkeystrokemgr">ITfKeystrokeMgr</a>