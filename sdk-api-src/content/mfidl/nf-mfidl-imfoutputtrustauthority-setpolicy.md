---
UID: NF:mfidl.IMFOutputTrustAuthority.SetPolicy
title: IMFOutputTrustAuthority::SetPolicy (mfidl.h)
description: Sets one or more policy objects on the output trust authority (OTA).
helpviewer_keywords: ["IMFOutputTrustAuthority interface [Media Foundation]","SetPolicy method","IMFOutputTrustAuthority.SetPolicy","IMFOutputTrustAuthority::SetPolicy","SetPolicy","SetPolicy method [Media Foundation]","SetPolicy method [Media Foundation]","IMFOutputTrustAuthority interface","f5102ef3-472f-4a38-889c-e1c25dd46765","mf.imfoutputtrustauthority_setpolicy","mfidl/IMFOutputTrustAuthority::SetPolicy"]
old-location: mf\imfoutputtrustauthority_setpolicy.htm
tech.root: mf
ms.assetid: f5102ef3-472f-4a38-889c-e1c25dd46765
ms.date: 12/05/2018
ms.keywords: IMFOutputTrustAuthority interface [Media Foundation],SetPolicy method, IMFOutputTrustAuthority.SetPolicy, IMFOutputTrustAuthority::SetPolicy, SetPolicy, SetPolicy method [Media Foundation], SetPolicy method [Media Foundation],IMFOutputTrustAuthority interface, f5102ef3-472f-4a38-889c-e1c25dd46765, mf.imfoutputtrustauthority_setpolicy, mfidl/IMFOutputTrustAuthority::SetPolicy
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFOutputTrustAuthority::SetPolicy
 - mfidl/IMFOutputTrustAuthority::SetPolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFOutputTrustAuthority.SetPolicy
---

# IMFOutputTrustAuthority::SetPolicy


## -description

Sets one or more policy objects on the output trust authority (OTA).

## -parameters

### -param ppPolicy [in]

The address of  an array of <a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy">IMFOutputPolicy</a> pointers.

### -param nPolicy [in]

The number of elements in the <i>ppPolicy</i> array.

### -param ppbTicket [out]

Receives either a pointer to a buffer allocated by the OTA, or the value <b>NULL</b>. If this parameter receives a non-<b>NULL</b> value, the caller must release the buffer by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. 

<div class="alert"><b>Note</b>  Currently this parameter is reserved. An OTA should set the pointer to <b>NULL</b>.</div>
<div> </div>

### -param pcbTicket [out]

Receives the size of the <i>ppbTicket</i> buffer, in bytes. If <i>ppbTicket</i> receives the value <b>NULL</b>, <i>pcbTicket</i> receives the value zero.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_S_WAIT_FOR_POLICY_SET</b></dt>
</dl>
</td>
<td width="60%">
The policy was negotiated successfully, but the OTA will enforce it asynchronously.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_POLICY_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The OTA does not support the requirements of this policy.
              

</td>
</tr>
</table>

## -remarks

If the method returns <b>MF_S_WAIT_FOR_POLICY_SET</b>, the OTA sends an <a href="/windows/desktop/medfound/mepolicyset">MEPolicySet</a> event when it enforces the policy.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority">IMFOutputTrustAuthority</a>