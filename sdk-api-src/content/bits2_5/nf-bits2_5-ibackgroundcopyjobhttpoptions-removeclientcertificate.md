---
UID: NF:bits2_5.IBackgroundCopyJobHttpOptions.RemoveClientCertificate
title: IBackgroundCopyJobHttpOptions::RemoveClientCertificate
author: windows-sdk-content
description: Removes the client certificate from the job.
old-location: bits\ibackgroundcopyjobhttpoptions_removeclientcertificate.htm
tech.root: bits
ms.assetid: b4fb7213-5f6b-407f-bc44-6d11886ed5ad
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IBackgroundCopyJobHttpOptions interface [BITS],RemoveClientCertificate method, IBackgroundCopyJobHttpOptions.RemoveClientCertificate, IBackgroundCopyJobHttpOptions::RemoveClientCertificate, RemoveClientCertificate, RemoveClientCertificate method [BITS], RemoveClientCertificate method [BITS],IBackgroundCopyJobHttpOptions interface, bits.ibackgroundcopyjobhttpoptions_removeclientcertificate, bits2_5/IBackgroundCopyJobHttpOptions::RemoveClientCertificate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJobHttpOptions::RemoveClientCertificate


## -description


Removes the client certificate from the job.


## -parameters






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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Successfully removed the certificate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_FALSE</b></b></dt>
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



You use the <a href="https://msdn.microsoft.com/60839bac-7f5f-4c43-84d4-26f1b21f974d">IBackgroundCopyJobHttpOptions::SetClientCertificateByID</a> or <a href="https://msdn.microsoft.com/8262b360-ab05-42a3-b5e7-178dc9f23fc6">IBackgroundCopyJobHttpOptions::SetClientCertificateByName</a> method to specify the certificate.




## -see-also




<a href="https://msdn.microsoft.com/d8ccf65d-a4f1-44d9-9903-43e5529f1f29">IBackgroundCopyJobHttpOptions</a>



<a href="https://msdn.microsoft.com/cd317bf9-1d4b-438e-beec-15ea7da90fc9">IBackgroundCopyJobHttpOptions::GetClientCertificate</a>



<a href="https://msdn.microsoft.com/60839bac-7f5f-4c43-84d4-26f1b21f974d">IBackgroundCopyJobHttpOptions::SetClientCertificateByID</a>



<a href="https://msdn.microsoft.com/8262b360-ab05-42a3-b5e7-178dc9f23fc6">IBackgroundCopyJobHttpOptions::SetClientCertificateByName</a>
 

 

