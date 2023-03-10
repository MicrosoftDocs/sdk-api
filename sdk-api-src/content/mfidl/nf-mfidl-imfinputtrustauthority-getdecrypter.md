---
UID: NF:mfidl.IMFInputTrustAuthority.GetDecrypter
title: IMFInputTrustAuthority::GetDecrypter (mfidl.h)
description: Retrieves a decrypter transform.
helpviewer_keywords: ["3bc4e2e6-41a8-4751-a7fe-5e1f8c136983","GetDecrypter","GetDecrypter method [Media Foundation]","GetDecrypter method [Media Foundation]","IMFInputTrustAuthority interface","IMFInputTrustAuthority interface [Media Foundation]","GetDecrypter method","IMFInputTrustAuthority.GetDecrypter","IMFInputTrustAuthority::GetDecrypter","mf.imfinputtrustauthority_getdecrypter","mfidl/IMFInputTrustAuthority::GetDecrypter"]
old-location: mf\imfinputtrustauthority_getdecrypter.htm
tech.root: mf
ms.assetid: 3bc4e2e6-41a8-4751-a7fe-5e1f8c136983
ms.date: 12/05/2018
ms.keywords: 3bc4e2e6-41a8-4751-a7fe-5e1f8c136983, GetDecrypter, GetDecrypter method [Media Foundation], GetDecrypter method [Media Foundation],IMFInputTrustAuthority interface, IMFInputTrustAuthority interface [Media Foundation],GetDecrypter method, IMFInputTrustAuthority.GetDecrypter, IMFInputTrustAuthority::GetDecrypter, mf.imfinputtrustauthority_getdecrypter, mfidl/IMFInputTrustAuthority::GetDecrypter
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
 - IMFInputTrustAuthority::GetDecrypter
 - mfidl/IMFInputTrustAuthority::GetDecrypter
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
 - IMFInputTrustAuthority.GetDecrypter
---

# IMFInputTrustAuthority::GetDecrypter


## -description

Retrieves a decrypter transform.

## -parameters

### -param riid [in]

Interface identifier (IID) of the interface being requested. Currently this value must be IID_IMFTransform, which requests the <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a> interface.

### -param ppv [out]

Receives a pointer to the interface. The caller must release the interface.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The decrypter does not support the requested interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_PROTECTED</b></dt>
</dl>
</td>
<td width="60%">
This input trust authority (ITA) does not provide a decrypter.

</td>
</tr>
</table>

## -remarks

The decrypter should be created in a disabled state, where any calls to <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a> automatically fail. After the input trust authority (ITA) has verified that it is running inside the protected media path (PMP), the ITA should enable the decrypter.

An ITA is not required to provide a decrypter. If the source content is not encrypted, the method should return MF_E_NOT_PROTECTED. The PMP will then proceed without using a decrypter for that stream.

The ITA must create a new instance of its decrypter for each call to <b>GetDecrypter</b>. Do not return multiple references to the same decrypter. They must be separate instances because the Media Session might place them in two different branches of the topology.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfinputtrustauthority">IMFInputTrustAuthority</a>