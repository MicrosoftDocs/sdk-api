---
UID: NF:wintrust.WintrustSetRegPolicyFlags
title: WintrustSetRegPolicyFlags function (wintrust.h)
description: Sets policy flags for a policy provider.
helpviewer_keywords: ["WTPF_ALLOWONLYPERTRUST","WTPF_IGNOREEXPIRATION","WTPF_IGNOREREVOCATIONONTS","WTPF_IGNOREREVOKATION","WTPF_OFFLINEOKNBU_COM","WTPF_OFFLINEOKNBU_IND","WTPF_OFFLINEOK_COM","WTPF_OFFLINEOK_IND","WTPF_TESTCANBEVALID","WTPF_TRUSTTEST","WTPF_VERIFY_V1_OFF","WintrustSetRegPolicyFlags","WintrustSetRegPolicyFlags function [Security]","security.wintrustsetregpolicyflags","wintrust/WintrustSetRegPolicyFlags"]
old-location: security\wintrustsetregpolicyflags.htm
tech.root: security
ms.assetid: 8aaeecd0-3814-42a0-9e5b-82b0b220bc9a
ms.date: 12/05/2018
ms.keywords: WTPF_ALLOWONLYPERTRUST, WTPF_IGNOREEXPIRATION, WTPF_IGNOREREVOCATIONONTS, WTPF_IGNOREREVOKATION, WTPF_OFFLINEOKNBU_COM, WTPF_OFFLINEOKNBU_IND, WTPF_OFFLINEOK_COM, WTPF_OFFLINEOK_IND, WTPF_TESTCANBEVALID, WTPF_TRUSTTEST, WTPF_VERIFY_V1_OFF, WintrustSetRegPolicyFlags, WintrustSetRegPolicyFlags function [Security], security.wintrustsetregpolicyflags, wintrust/WintrustSetRegPolicyFlags
req.header: wintrust.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wintrust.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WintrustSetRegPolicyFlags
 - wintrust/WintrustSetRegPolicyFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - WintrustSetRegPolicyFlags
---

# WintrustSetRegPolicyFlags function


## -description

The <b>WintrustSetRegPolicyFlags</b> function sets policy flags for a policy provider.
<div class="alert"><b>Note</b>  This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.</div><div> </div>

## -parameters

### -param dwPolicyFlags [in]

This parameter can be a bitwise combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WTPF_TRUSTTEST"></a><a id="wtpf_trusttest"></a><dl>
<dt><b>WTPF_TRUSTTEST</b></dt>
</dl>
</td>
<td width="60%">
Trust any test certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_TESTCANBEVALID"></a><a id="wtpf_testcanbevalid"></a><dl>
<dt><b>WTPF_TESTCANBEVALID</b></dt>
</dl>
</td>
<td width="60%">
Check any test certificate for validity.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_IGNOREEXPIRATION"></a><a id="wtpf_ignoreexpiration"></a><dl>
<dt><b>WTPF_IGNOREEXPIRATION</b></dt>
</dl>
</td>
<td width="60%">
Do not check the  expiration date.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_IGNOREREVOKATION"></a><a id="wtpf_ignorerevokation"></a><dl>
<dt><b>WTPF_IGNOREREVOKATION</b></dt>
</dl>
</td>
<td width="60%">
Do not check revocation.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_OFFLINEOK_IND"></a><a id="wtpf_offlineok_ind"></a><dl>
<dt><b>WTPF_OFFLINEOK_IND</b></dt>
</dl>
</td>
<td width="60%">
If the source is offline, trust any individual certificates.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_OFFLINEOK_COM"></a><a id="wtpf_offlineok_com"></a><dl>
<dt><b>WTPF_OFFLINEOK_COM</b></dt>
</dl>
</td>
<td width="60%">
If the source is offline, trust any commercial certificates.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_OFFLINEOKNBU_IND"></a><a id="wtpf_offlineoknbu_ind"></a><dl>
<dt><b>WTPF_OFFLINEOKNBU_IND</b></dt>
</dl>
</td>
<td width="60%">
If the source is offline, trust any individual certificates. Do not use the user interface (UI).

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_OFFLINEOKNBU_COM"></a><a id="wtpf_offlineoknbu_com"></a><dl>
<dt><b>WTPF_OFFLINEOKNBU_COM</b></dt>
</dl>
</td>
<td width="60%">
If the source is offline, trust any commercial certificates. Do not use the checking UI.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_VERIFY_V1_OFF"></a><a id="wtpf_verify_v1_off"></a><dl>
<dt><b>WTPF_VERIFY_V1_OFF</b></dt>
</dl>
</td>
<td width="60%">
Turn off verification of version 1.0 certificates.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_IGNOREREVOCATIONONTS"></a><a id="wtpf_ignorerevocationonts"></a><dl>
<dt><b>WTPF_IGNOREREVOCATIONONTS</b></dt>
</dl>
</td>
<td width="60%">
Ignore time stamp revocation checks.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_ALLOWONLYPERTRUST"></a><a id="wtpf_allowonlypertrust"></a><dl>
<dt><b>WTPF_ALLOWONLYPERTRUST</b></dt>
</dl>
</td>
<td width="60%">
Allow only items in personal trust database.

</td>
</tr>
</table>

## -returns

Returns nonzero if the policy flags were set successfully or zero otherwise.

## -see-also

<a href="/windows/desktop/api/wintrust/nf-wintrust-wintrustgetregpolicyflags">WintrustGetRegPolicyFlags</a>