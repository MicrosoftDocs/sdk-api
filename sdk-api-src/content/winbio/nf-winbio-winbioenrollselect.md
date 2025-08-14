---
UID: NF:winbio.WinBioEnrollSelect
title: WinBioEnrollSelect function (winbio.h)
description: Specifies the individual that you want to enroll when data that represents multiple individuals is present in the sample buffer. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
helpviewer_keywords: ["WinBioEnrollSelect","WinBioEnrollSelect function [Windows Biometric Framework API]","secbiomet.winbioenrollselect","winbio/WinBioEnrollSelect"]
old-location: secbiomet\winbioenrollselect.htm
tech.root: SecBioMet
ms.assetid: 9C06B976-9B60-43B6-B68B-255A6882912B
ms.date: 12/05/2018
ms.keywords: WinBioEnrollSelect, WinBioEnrollSelect function [Windows Biometric Framework API], secbiomet.winbioenrollselect, winbio/WinBioEnrollSelect
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
 - WinBioEnrollSelect
 - winbio/WinBioEnrollSelect
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
 - WinBioEnrollSelect
---

# WinBioEnrollSelect function


## -description

Specifies the individual  that you want to enroll when data that represents multiple individuals is present in the sample buffer. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.

## -parameters

### -param SessionHandle [in]

A <b>WINBIO_SESSION_HANDLE</b> value that identifies an open biometric session.  Open a synchronous session handle by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>. Open an asynchronous session handle by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>.

For enrollment in facial recognition, use <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a> with the <i>PoolType</i> parameter set to <b>WINBIO_POOL_SYSTEM</b> to get the handle.

### -param SelectorValue [in]

A value that identifies that individual that you want to select for enrollment.

## -returns

If the function succeeds, it returns S_OK. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_HANDLE</b></b></dt>
</dl>
</td>
<td width="60%">
The session handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_INVALIDARG</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>SelectorValue</i> parameter cannot equal zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_INCORRECT_SESSION_TYPE</b></b></dt>
</dl>
</td>
<td width="60%">
The session handle does not correspond to a biometric session.

</td>
</tr>
</table>

## -remarks

For enrollment in facial recognition, you can find the correct selector value in either of two ways:

<ul>
<li>The value of the <b>Id</b> member of one of the <a href="/windows/desktop/SecBioMet/winbio-presence">WINBIO_PRESENCE</a> structures previously sent.</li>
<li>The data produced by the NUI face-tracking APIs.</li>
</ul>
Call <b>WinBioEnrollSelect</b> to set the selector value after you call <a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollbegin">WinBioEnrollBegin</a> to start an enrollment sequence. The selector value applies to all subsequent <a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollcapture">WinBioEnrollCapture</a> calls. The selection setting is temporary and is automatically cleared when you finish the enrollment sequence by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollcommit">WinBioEnrollCommit</a> or <a href="/windows/desktop/api/winbio/nf-winbio-winbioenrolldiscard">WinBioEnrollDiscard</a>.

If you call <b>WinBioEnrollSelect</b> for biometric factors that do not require disambiguation, such as fingerprints, the return value for the function indicates success, but function ignores the selector value.

If you do not call <b>WinBioEnrollSelect</b> for a biometric factor that requires you to call the function, subsequent calls to <a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollcapture">WinBioEnrollCapture</a> fail with the  <b>WINBIO_E_SELECTION_REQUIRED</b> error. 

 For Windows 10, the factors that require you to call <b>WinBioEnrollSelect</b> are facial features and iris.

You can call <b>WinBioEnrollSelect</b> by using either a synchronous or asynchronous session handle. As with other calls to Windows Biometric Framework API functions, when you call <b>WinBioEnrollSelect</b>  with an asynchronous session handle, the return value indicates only that the function parameters were acceptable. The actual success or failure of the operation itself will be returned to your notification routine in a <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure.

## -see-also

<a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a>



<a href="/windows/desktop/SecBioMet/winbio-presence">WINBIO_PRESENCE</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollbegin">WinBioEnrollBegin</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollcapture">WinBioEnrollCapture</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollcommit">WinBioEnrollCommit</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenrolldiscard">WinBioEnrollDiscard</a>