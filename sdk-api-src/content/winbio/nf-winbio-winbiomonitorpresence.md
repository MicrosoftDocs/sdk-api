---
UID: NF:winbio.WinBioMonitorPresence
title: WinBioMonitorPresence function (winbio.h)
description: Turns on the face-recognition or iris-monitoring mechanism for the specified biometric unit. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
helpviewer_keywords: ["WinBioMonitorPresence","WinBioMonitorPresence function [Windows Biometric Framework API]","secbiomet.winbiomonitorpresence","winbio/WinBioMonitorPresence"]
old-location: secbiomet\winbiomonitorpresence.htm
tech.root: SecBioMet
ms.assetid: 973DA92D-7319-43A9-B4FF-3CAF8A644C50
ms.date: 12/05/2018
ms.keywords: WinBioMonitorPresence, WinBioMonitorPresence function [Windows Biometric Framework API], secbiomet.winbiomonitorpresence, winbio/WinBioMonitorPresence
req.header: winbio.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinBioMonitorPresence
 - winbio/WinBioMonitorPresence
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-biometrics-winbio-core-l1-1-6.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-5.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-4.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-3.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-2.dll
 - winbio.dll
 - Ext-MS-Win-Biometrics-WinBio-Core-L1-1-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
 - WinBioMonitorPresence
---

# WinBioMonitorPresence function


## -description

Turns on the face-recognition or iris-monitoring mechanism for the specified biometric unit. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.

## -parameters

### -param SessionHandle [in]

An asynchronous handle for the biometric session that you obtained by  calling the <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a> function with the <i>PoolType</i> parameter set to <b>WINBIO_POOL_SYSTEM</b>.

### -param UnitId [in]

The identifier of the biometric unit for which you want to turn on the  face-recognition or iris-monitoring mechanism.

## -returns

If the function parameters are acceptable, it returns <b>S_OK</b>. If the function parameters are not acceptable, it returns an <b>HRESULT</b> value that indicates the error.  
Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The session handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>UnitId</i> parameter cannot equal zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INCORRECT_SESSION_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The session handle does not correspond to an asynchronous biometric session.

</td>
</tr>
</table>
 

The actual success or failure of the operation itself is returned to the your notification function in a <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure.

## -remarks

A single biometric session can have only one active presence monitor at any point in time.

After you successfully call <b>WinBioMonitorPresence</b>, your notification  function receives notifications in the form of a <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure with an <b>Operation</b> member equal to <b>WINBIO_OPERATION_MONITOR_PRESENCE</b>. You should then examine the <b>Parameters.MonitorPresence</b> member of the <b>WINBIO_ASYNC_RESULT</b> structure for more information.

To stop receiving notifications, call either <a href="/windows/desktop/api/winbio/nf-winbio-winbiocancel">WinBioCancel</a> or <a href="/windows/desktop/api/winbio/nf-winbio-winbioclosesession">WinBioCloseSession</a> with the original asynchronous handle value.

## -see-also

<a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbiocancel">WinBioCancel</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioclosesession">WinBioCloseSession</a>