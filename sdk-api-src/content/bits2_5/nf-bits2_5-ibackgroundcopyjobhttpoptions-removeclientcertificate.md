---
UID: NF:bits2_5.IBackgroundCopyJobHttpOptions.RemoveClientCertificate
title: IBackgroundCopyJobHttpOptions::RemoveClientCertificate (bits2_5.h)
description: Removes the client certificate from the job.
helpviewer_keywords: ["IBackgroundCopyJobHttpOptions interface [BITS]","RemoveClientCertificate method","IBackgroundCopyJobHttpOptions.RemoveClientCertificate","IBackgroundCopyJobHttpOptions::RemoveClientCertificate","RemoveClientCertificate","RemoveClientCertificate method [BITS]","RemoveClientCertificate method [BITS]","IBackgroundCopyJobHttpOptions interface","bits.ibackgroundcopyjobhttpoptions_removeclientcertificate","bits2_5/IBackgroundCopyJobHttpOptions::RemoveClientCertificate"]
old-location: bits\ibackgroundcopyjobhttpoptions_removeclientcertificate.htm
tech.root: Bits
ms.assetid: b4fb7213-5f6b-407f-bc44-6d11886ed5ad
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJobHttpOptions interface [BITS],RemoveClientCertificate method, IBackgroundCopyJobHttpOptions.RemoveClientCertificate, IBackgroundCopyJobHttpOptions::RemoveClientCertificate, RemoveClientCertificate, RemoveClientCertificate method [BITS], RemoveClientCertificate method [BITS],IBackgroundCopyJobHttpOptions interface, bits.ibackgroundcopyjobhttpoptions_removeclientcertificate, bits2_5/IBackgroundCopyJobHttpOptions::RemoveClientCertificate
req.header: bits2_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits2_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJobHttpOptions::RemoveClientCertificate
 - bits2_5/IBackgroundCopyJobHttpOptions::RemoveClientCertificate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyJobHttpOptions.RemoveClientCertificate
---

# IBackgroundCopyJobHttpOptions::RemoveClientCertificate


## -description

Removes the client certificate from the job.



## -returns

The following table lists some of the possible return values.

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
Successfully removed the certificate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The job does not specify a certificate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.

</td>
</tr>
</table>

## -remarks

You use the <a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid">IBackgroundCopyJobHttpOptions::SetClientCertificateByID</a> or <a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname">IBackgroundCopyJobHttpOptions::SetClientCertificateByName</a> method to specify the certificate.

## -see-also

<a href="/windows/desktop/api/bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions">IBackgroundCopyJobHttpOptions</a>



<a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-getclientcertificate">IBackgroundCopyJobHttpOptions::GetClientCertificate</a>



<a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid">IBackgroundCopyJobHttpOptions::SetClientCertificateByID</a>



<a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname">IBackgroundCopyJobHttpOptions::SetClientCertificateByName</a>
