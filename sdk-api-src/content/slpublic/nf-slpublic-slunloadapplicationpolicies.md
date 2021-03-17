---
UID: NF:slpublic.SLUnloadApplicationPolicies
title: SLUnloadApplicationPolicies function (slpublic.h)
description: Releases the policy context handle returned by the SLLoadApplicationPolicies function.
helpviewer_keywords: ["SLUnloadApplicationPolicies","SLUnloadApplicationPolicies function [Security]","security.slunloadapplicationpolicies","slpublic/SLUnloadApplicationPolicies"]
old-location: security\slunloadapplicationpolicies.htm
tech.root: security
ms.assetid: 56dae943-659a-4e75-81ef-0d58fa3cd6d2
ms.date: 12/05/2018
ms.keywords: SLUnloadApplicationPolicies, SLUnloadApplicationPolicies function [Security], security.slunloadapplicationpolicies, slpublic/SLUnloadApplicationPolicies
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - SLUnloadApplicationPolicies
 - slpublic/SLUnloadApplicationPolicies
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
 - SLUnloadApplicationPolicies
---

# SLUnloadApplicationPolicies function


## -description

Releases the policy context handle returned by the <a href="/windows/desktop/api/slpublic/nf-slpublic-slloadapplicationpolicies">SLLoadApplicationPolicies</a> function.

## -parameters

### -param hPolicyContext [in]

Type: <b>HSLP</b>

The context handle returned by the <a href="/windows/desktop/api/slpublic/nf-slpublic-slloadapplicationpolicies">SLLoadApplicationPolicies</a> function.

### -param dwFlags [in]

Type: <b>DWORD</b>

The additional flags.

## -returns

Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise, it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_APPLICATION_POLICIES_NOT_LOADED</b></dt>
<dt>0xC004F073</dt>
</dl>
</td>
<td width="60%">
The policy context was not found.

</td>
</tr>
</table>