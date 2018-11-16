---
UID: NN:msopc.IOpcCertificateSet
title: IOpcCertificateSet
author: windows-sdk-content
description: An unordered set of certificates to be used with a signature.
old-location: opc\iopccertificateset.htm
tech.root: OPC
ms.assetid: 0ac56b41-a120-4a9b-9bfa-afba1ba0f3b4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOpcCertificateSet, IOpcCertificateSet interface [Open Packaging Conventions], IOpcCertificateSet interface [Open Packaging Conventions],described, msopc/IOpcCertificateSet, opc.iopccertificateset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcCertificateSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcCertificateSet interface


## -description


An unordered set of certificates to be used with a signature.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcCertificateSet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcCertificateSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcCertificateSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d14e9a1e-dda3-4b57-9882-0fd473a19e8c">Add</a>
</td>
<td align="left" width="63%">
Adds a certificate to the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a48b9225-07cb-4367-b011-dc2297c2c4b3">GetEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of certificates in the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15046223-f8a0-4810-b6e0-e75aca44d5a9">Remove</a>
</td>
<td align="left" width="63%">
Removes a specified certificate from the set.

</td>
</tr>
</table> 


## -remarks



Do not add the certificate that will be passed to the <a href="https://msdn.microsoft.com/5d40cae4-67d5-40a6-bd63-cf6243a703eb">IOpcDigitalSignature::Sign</a> method (the signer certificate) to this certificate set.

Certificates that are in a certificate chain are added to the package by calling the <a href="https://msdn.microsoft.com/d14e9a1e-dda3-4b57-9882-0fd473a19e8c">Add</a> method.

To access an <b>IOpcCertificateSet</b> interface pointer, call the <a href="https://msdn.microsoft.com/df212397-7ec9-4a42-bebb-61799b7ca78e">IOpcSigningOptions::GetCertificateSet</a> method.

When a signature is generated, certificates that were added to the package by calling <a href="https://msdn.microsoft.com/d14e9a1e-dda3-4b57-9882-0fd473a19e8c">Add</a> are associated  with the signature.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="http://msdn.microsoft.com/en-us/library/aa377189(vs.85).aspx">CERT_CONTEXT</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376489(v=VS.85).aspx">Certificates</a>



<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/a66ad728-9d20-44d9-a363-1d2a7927d810">IOpcCertificateEnumerator</a>



<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

