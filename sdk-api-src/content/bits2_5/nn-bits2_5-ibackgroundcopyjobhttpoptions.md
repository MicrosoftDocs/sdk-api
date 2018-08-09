---
UID: NN:bits2_5.IBackgroundCopyJobHttpOptions
title: IBackgroundCopyJobHttpOptions
author: windows-sdk-content
description: Use this interface to specify client certificates for certificate-based client authentication and custom headers for HTTP requests.
old-location: bits\ibackgroundcopyjobhttpoptions.htm
old-project: bits
ms.assetid: d8ccf65d-a4f1-44d9-9903-43e5529f1f29
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IBackgroundCopyJobHttpOptions, IBackgroundCopyJobHttpOptions interface [BITS], IBackgroundCopyJobHttpOptions interface [BITS],described, bits.ibackgroundcopyjobhttpoptions, bits2_5/IBackgroundCopyJobHttpOptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: BG_CERT_STORE_LOCATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx4.dll
api_name:
 - IBackgroundCopyJobHttpOptions
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: BitsPrx4.dll
req.irql: 
---

# IBackgroundCopyJobHttpOptions interface


## -description


Use this interface to specify client certificates for certificate-based client authentication and custom headers for HTTP requests. 

To get this interface, call the <b>IBackgroundCopyJob::QueryInterface</b> method using __uuidof(IBackgroundCopyJobHttpOptions) for the interface identifier. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyJobHttpOptions</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBackgroundCopyJobHttpOptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyJobHttpOptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd317bf9-1d4b-438e-beec-15ea7da90fc9">GetClientCertificate</a>
</td>
<td align="left" width="63%">
Retrieves the client certificate from the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8be6e9ec-7c74-44ff-94d7-a1a1d7fb18e9">GetCustomHeaders</a>
</td>
<td align="left" width="63%">
Retrieves the custom HTTP headers from the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75104dca-086e-45f6-ad9e-a96730b37433">GetSecurityFlags</a>
</td>
<td align="left" width="63%">
Retrieves the flags for HTTP that determine whether the certificate revocation list is checked and certain certificate errors are ignored, and the policy to use when a server redirects the HTTP request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4fb7213-5f6b-407f-bc44-6d11886ed5ad">RemoveClientCertificate</a>
</td>
<td align="left" width="63%">
Removes the client certificate from the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60839bac-7f5f-4c43-84d4-26f1b21f974d">SetClientCertificateByID</a>
</td>
<td align="left" width="63%">
Specifies the identifier of the client certificate to use for client authentication in an HTTPS (SSL) request. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8262b360-ab05-42a3-b5e7-178dc9f23fc6">SetClientCertificateByName</a>
</td>
<td align="left" width="63%">
Specifies the subject name of the client certificate to use for client authentication in an HTTPS (SSL) request. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/422a331d-5b6b-48ec-b040-43a88be43ac3">SetCustomHeaders</a>
</td>
<td align="left" width="63%">
Specifies one or more custom HTTP headers to include in HTTP requests.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/afac84cb-28ab-4c80-ab39-eefe450ae3e5">SetSecurityFlags</a>
</td>
<td align="left" width="63%">
Sets flags for HTTP that determine whether the certificate revocation list is checked and certain certificate errors are ignored, and the policy to use when a server redirects the HTTP request.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a>
 

 

