---
UID: NN:msopc.IOpcCertificateEnumerator
title: IOpcCertificateEnumerator (msopc.h)
author: windows-sdk-content
description: A read-only enumerator of pointers to CERT_CONTEXT structures.
old-location: opc\iopccertificateenumerator.htm
tech.root: OPC
ms.assetid: a66ad728-9d20-44d9-a363-1d2a7927d810
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOpcCertificateEnumerator, IOpcCertificateEnumerator interface [Open Packaging Conventions], IOpcCertificateEnumerator interface [Open Packaging Conventions],described, msopc/IOpcCertificateEnumerator, opc.iopccertificateenumerator
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
 - IOpcCertificateEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcCertificateEnumerator interface


## -description


A read-only enumerator of pointers to <a href="http://msdn.microsoft.com/en-us/library/aa377189(vs.85).aspx">CERT_CONTEXT</a> structures.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcCertificateEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcCertificateEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcCertificateEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cf4bed8-4a6f-48f4-b72f-a13efc127b2a">Clone</a>
</td>
<td align="left" width="63%">
              Creates a copy of the current <b>IOpcCertificateEnumerator</b> interface pointer and all its descendants.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/edd2afc1-cafd-4a52-b2df-1a1fcdf1d6fa">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the <a href="http://msdn.microsoft.com/en-us/library/aa377189(vs.85).aspx">CERT_CONTEXT</a> structure at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81918b97-0d10-4d7c-aaad-fc886d55e664">MoveNext</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the next <a href="http://msdn.microsoft.com/en-us/library/aa377189(vs.85).aspx">CERT_CONTEXT</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/564c391c-8c73-4dd8-b713-3a5309708fd6">MovePrevious</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the previous <a href="http://msdn.microsoft.com/en-us/library/aa377189(vs.85).aspx">CERT_CONTEXT</a> structure.

</td>
</tr>
</table> 


## -remarks



When an enumerator is created, the current position precedes the first pointer of the enumerator. To set the current position to the first pointer, call the  <a href="https://msdn.microsoft.com/81918b97-0d10-4d7c-aaad-fc886d55e664">MoveNext</a>method after the enumerator is created.

Changes to the set will invalidate the enumerator and all subsequent calls to it will fail.

To get an <b>IOpcCertificateEnumerator</b> interface pointer, call the  <a href="https://msdn.microsoft.com/a48b9225-07cb-4367-b011-dc2297c2c4b3">IOpcCertificateSet::GetEnumerator</a> or <a href="https://msdn.microsoft.com/5b5b803f-fc61-41fa-aa73-eefb1c1d2f00">IOpcDigitalSignature::GetCertificateEnumerator</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376489(v=VS.85).aspx">Certificates</a>



<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/0ac56b41-a120-4a9b-9bfa-afba1ba0f3b4">IOpcCertificateSet</a>



<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

