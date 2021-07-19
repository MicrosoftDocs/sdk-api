---
UID: NF:mfidl.IMFInputTrustAuthority.Reset
title: IMFInputTrustAuthority::Reset (mfidl.h)
description: Resets the input trust authority (ITA) to its initial state.
helpviewer_keywords: ["IMFInputTrustAuthority interface [Media Foundation]","Reset method","IMFInputTrustAuthority.Reset","IMFInputTrustAuthority::Reset","Reset","Reset method [Media Foundation]","Reset method [Media Foundation]","IMFInputTrustAuthority interface","beb8e598-5a35-46b0-aa13-6bef38b9defb","mf.imfinputtrustauthority_reset","mfidl/IMFInputTrustAuthority::Reset"]
old-location: mf\imfinputtrustauthority_reset.htm
tech.root: mf
ms.assetid: beb8e598-5a35-46b0-aa13-6bef38b9defb
ms.date: 12/05/2018
ms.keywords: IMFInputTrustAuthority interface [Media Foundation],Reset method, IMFInputTrustAuthority.Reset, IMFInputTrustAuthority::Reset, Reset, Reset method [Media Foundation], Reset method [Media Foundation],IMFInputTrustAuthority interface, beb8e598-5a35-46b0-aa13-6bef38b9defb, mf.imfinputtrustauthority_reset, mfidl/IMFInputTrustAuthority::Reset
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
 - IMFInputTrustAuthority::Reset
 - mfidl/IMFInputTrustAuthority::Reset
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
 - IMFInputTrustAuthority.Reset
---

# IMFInputTrustAuthority::Reset


## -description

Resets the input trust authority (ITA) to its initial state.



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
</table>

## -remarks

When this method is called, the ITA should disable any decrypter that was returned in the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter">IMFInputTrustAuthority::GetDecrypter</a> method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfinputtrustauthority">IMFInputTrustAuthority</a>
