---
UID: NF:slpublic.SLGetGenuineInformation
title: SLGetGenuineInformation function (slpublic.h)
description: Gets information about the genuine state of a Windows computer.
helpviewer_keywords: ["SLGetGenuineInformation","SLGetGenuineInformation function [Security]","SL_BRT_COMMIT","SL_BRT_DATA","SL_GENUINE_RESULT","SL_NONGENUINE_GRACE_FLAG","security.slgetgenuineinformation","slpublic/SLGetGenuineInformation"]
old-location: security\slgetgenuineinformation.htm
tech.root: security
ms.assetid: 8dcc6ef1-1839-49c6-8119-1e3a8135fce2
ms.date: 12/05/2018
ms.keywords: SLGetGenuineInformation, SLGetGenuineInformation function [Security], SL_BRT_COMMIT, SL_BRT_DATA, SL_GENUINE_RESULT, SL_NONGENUINE_GRACE_FLAG, security.slgetgenuineinformation, slpublic/SLGetGenuineInformation
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SLGetGenuineInformation
 - slpublic/SLGetGenuineInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Slc.dll
api_name:
 - SLGetGenuineInformation
---

# SLGetGenuineInformation function


## -description

Gets information about the genuine state of a Windows computer.

## -parameters

### -param pQueryId [in]

A pointer to an <b>SLID</b> structure that specifies the application to check.

### -param pwszValueName [in]

A pointer to a null-terminated string that contains the name associated with the value to retrieve. The following names are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SL_BRT_DATA"></a><a id="sl_brt_data"></a><dl>
<dt><b>SL_BRT_DATA</b></dt>
</dl>
</td>
<td width="60%">
Get a value that specifies whether the computer is genuine.

</td>
</tr>
<tr>
<td width="40%"><a id="SL_BRT_COMMIT"></a><a id="sl_brt_commit"></a><dl>
<dt><b>SL_BRT_COMMIT</b></dt>
</dl>
</td>
<td width="60%">
Get a value that specifies whether the computer is in nongenuine grace period mode.

</td>
</tr>
<tr>
<td width="40%"><a id="SL_GENUINE_RESULT"></a><a id="sl_genuine_result"></a><dl>
<dt><b>SL_GENUINE_RESULT</b></dt>
</dl>
</td>
<td width="60%">
Get the value returned from the last call to the <a href="/windows/desktop/api/slpublic/nf-slpublic-slacquiregenuineticket">SLAcquireGenuineTicket</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="SL_NONGENUINE_GRACE_FLAG"></a><a id="sl_nongenuine_grace_flag"></a><dl>
<dt><b>SL_NONGENUINE_GRACE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Gets the cause of the computer being put into nongenuine grace period mode.

</td>
</tr>
</table>

### -param peDataType [out, optional]

A pointer to a value of the <a href="/windows/desktop/api/slpublic/ne-slpublic-sldatatype">SLDATATYPE</a> enumeration that specifies the type of data in the <i>ppbValue</i> buffer.

### -param pcbValue [out]

A pointer to the size, in bytes, of the <i>ppbValue</i> buffer.

### -param ppbValue [out]

The address of a pointer to an array of <b>BYTE</b> pointers that specifies the value associated with the name specified by the <i>pwszValueName</i> parameter.

When you have finished using this array, free it by calling the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

This function can return the following values defined in Slerror.h.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_NOT_SUPPORTED</b></dt>
<dt>0xC004F016</dt>
</dl>
</td>
<td width="60%">
The name specified by the <i>pwszValueName</i> parameter is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_VALUE_NOT_FOUND</b></dt>
<dt>0xC004F012</dt>
</dl>
</td>
<td width="60%">
The specified name-value pair was not found.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/slpublic/ne-slpublic-sldatatype">SLDATATYPE</a>



<a href="/windows/desktop/api/slpublic/nf-slpublic-slgetwindowsinformation">SLGetWindowsInformation</a>