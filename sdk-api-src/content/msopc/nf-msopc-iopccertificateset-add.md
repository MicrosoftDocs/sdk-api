---
UID: NF:msopc.IOpcCertificateSet.Add
title: IOpcCertificateSet::Add
author: windows-sdk-content
description: Adds a certificate to the set.
old-location: opc\iopccertificateset_add.htm
tech.root: OPC
ms.assetid: d14e9a1e-dda3-4b57-9882-0fd473a19e8c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Add, Add method [Open Packaging Conventions], Add method [Open Packaging Conventions],IOpcCertificateSet interface, IOpcCertificateSet interface [Open Packaging Conventions],Add method, IOpcCertificateSet.Add, IOpcCertificateSet::Add, msopc/IOpcCertificateSet::Add, opc.iopccertificateset_add
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OpcDigitalSignature.idl
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
 - IOpcCertificateSet.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcCertificateSet::Add


## -description


Adds a certificate to the set.


## -parameters




### -param certificate [in]

A 
       <a href="http://msdn.microsoft.com/en-us/library/aa377189(vs.85).aspx">CERT_CONTEXT</a> 
       structure that contains the certificate to be added.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, 
       those in the following table.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>certificate</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Certificates that are in a certificate chain are added to the package by calling the 
    <b>Add</b> method.

When a signature is 
    generated, certificates that were added to the package by calling 
    <b>Add</b> are associated  with the signature.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the 
    <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="f15bc83f-43b0-4b09-9bb5-c668e901b864">Certificates</a>



<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/0ac56b41-a120-4a9b-9bfa-afba1ba0f3b4">IOpcCertificateSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

