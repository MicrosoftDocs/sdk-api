---
UID: NF:mfidl.IMFSecureChannel.GetCertificate
title: IMFSecureChannel::GetCertificate (mfidl.h)
description: Retrieves the client's certificate.
helpviewer_keywords: ["GetCertificate","GetCertificate method [Media Foundation]","GetCertificate method [Media Foundation]","IMFSecureChannel interface","IMFSecureChannel interface [Media Foundation]","GetCertificate method","IMFSecureChannel.GetCertificate","IMFSecureChannel::GetCertificate","d5465070-1706-4420-8351-fab5e8e8cd08","mf.imfsecurechannel_getcertificate","mfidl/IMFSecureChannel::GetCertificate"]
old-location: mf\imfsecurechannel_getcertificate.htm
tech.root: mf
ms.assetid: d5465070-1706-4420-8351-fab5e8e8cd08
ms.date: 12/05/2018
ms.keywords: GetCertificate, GetCertificate method [Media Foundation], GetCertificate method [Media Foundation],IMFSecureChannel interface, IMFSecureChannel interface [Media Foundation],GetCertificate method, IMFSecureChannel.GetCertificate, IMFSecureChannel::GetCertificate, d5465070-1706-4420-8351-fab5e8e8cd08, mf.imfsecurechannel_getcertificate, mfidl/IMFSecureChannel::GetCertificate
req.header: mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSecureChannel::GetCertificate
 - mfidl/IMFSecureChannel::GetCertificate
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
 - IMFSecureChannel.GetCertificate
---

# IMFSecureChannel::GetCertificate


## -description

Retrieves the client's certificate.

## -parameters

### -param ppCert [out]

Receives a pointer to a buffer allocated by the object. The buffer contains the client's certificate. The caller must release the buffer by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param pcbCert [out]

Receives the size of the <i>ppCert</i> buffer, in bytes.

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

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsecurechannel">IMFSecureChannel</a>