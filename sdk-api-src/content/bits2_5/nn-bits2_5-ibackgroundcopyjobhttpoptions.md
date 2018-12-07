---
UID: NN:bits2_5.IBackgroundCopyJobHttpOptions
title: IBackgroundCopyJobHttpOptions
author: windows-sdk-content
description: Use this interface to specify client certificates for certificate-based client authentication and custom headers for HTTP requests.
old-location: bits\ibackgroundcopyjobhttpoptions.htm
tech.root: bits
ms.assetid: d8ccf65d-a4f1-44d9-9903-43e5529f1f29
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBackgroundCopyJobHttpOptions, IBackgroundCopyJobHttpOptions interface [BITS], IBackgroundCopyJobHttpOptions interface [BITS],described, bits.ibackgroundcopyjobhttpoptions, bits2_5/IBackgroundCopyJobHttpOptions
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Bits.lib
req.dll: BitsPrx4.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# IBackgroundCopyJobHttpOptions interface


## -description


Use this interface to specify client certificates for certificate-based client authentication and custom headers for HTTP requests. 

To get this interface, call the <b>IBackgroundCopyJob::QueryInterface</b> method using __uuidof(IBackgroundCopyJobHttpOptions) for the interface identifier. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyJobHttpOptions</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IBackgroundCopyJobHttpOptions</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa964251(v=VS.85).aspx">GetClientCertificate</a>
</td>
<td align="left" width="63%">
Retrieves the client certificate from the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964252(v=VS.85).aspx">GetCustomHeaders</a>
</td>
<td align="left" width="63%">
Retrieves the custom HTTP headers from the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964253(v=VS.85).aspx">GetSecurityFlags</a>
</td>
<td align="left" width="63%">
Retrieves the flags for HTTP that determine whether the certificate revocation list is checked and certain certificate errors are ignored, and the policy to use when a server redirects the HTTP request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964255(v=VS.85).aspx">RemoveClientCertificate</a>
</td>
<td align="left" width="63%">
Removes the client certificate from the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964256(v=VS.85).aspx">SetClientCertificateByID</a>
</td>
<td align="left" width="63%">
Specifies the identifier of the client certificate to use for client authentication in an HTTPS (SSL) request. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964257(v=VS.85).aspx">SetClientCertificateByName</a>
</td>
<td align="left" width="63%">
Specifies the subject name of the client certificate to use for client authentication in an HTTPS (SSL) request. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964258(v=VS.85).aspx">SetCustomHeaders</a>
</td>
<td align="left" width="63%">
Specifies one or more custom HTTP headers to include in HTTP requests.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964260(v=VS.85).aspx">SetSecurityFlags</a>
</td>
<td align="left" width="63%">
Sets flags for HTTP that determine whether the certificate revocation list is checked and certain certificate errors are ignored, and the policy to use when a server redirects the HTTP request.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362973(v=VS.85).aspx">IBackgroundCopyJob</a>
 

 

