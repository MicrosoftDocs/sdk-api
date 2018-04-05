---
UID: NF:msopc.IOpcCertificateSet.GetEnumerator
title: IOpcCertificateSet::GetEnumerator method
author: windows-driver-content
description: Gets an enumerator of certificates in the set.
old-location: opc\iopccertificateset_getenumerator.htm
old-project: OPC
ms.assetid: a48b9225-07cb-4367-b011-dc2297c2c4b3
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetEnumerator method [Open Packaging Conventions], GetEnumerator method [Open Packaging Conventions], IOpcCertificateSet interface, GetEnumerator,IOpcCertificateSet.GetEnumerator, IOpcCertificateSet, IOpcCertificateSet interface [Open Packaging Conventions], GetEnumerator method, IOpcCertificateSet::GetEnumerator, msopc/IOpcCertificateSet::GetEnumerator, opc.iopccertificateset_getenumerator
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
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msopc.h
api_name:
-	IOpcCertificateSet.GetEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOpcCertificateSet::GetEnumerator method


## -description


Gets an enumerator of certificates in the set.


## -parameters




### -param certificateEnumerator [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/a66ad728-9d20-44d9-a363-1d2a7927d810">IOpcCertificateEnumerator</a> interface of certificates in the set.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>certificateEnumerator</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt484158">Certificates</a>



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
 

 

