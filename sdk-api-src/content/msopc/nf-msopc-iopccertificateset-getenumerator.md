---
UID: NF:msopc.IOpcCertificateSet.GetEnumerator
title: IOpcCertificateSet::GetEnumerator (msopc.h)
description: Gets an enumerator of certificates in the set.
helpviewer_keywords: ["GetEnumerator","GetEnumerator method [Open Packaging Conventions]","GetEnumerator method [Open Packaging Conventions]","IOpcCertificateSet interface","IOpcCertificateSet interface [Open Packaging Conventions]","GetEnumerator method","IOpcCertificateSet.GetEnumerator","IOpcCertificateSet::GetEnumerator","msopc/IOpcCertificateSet::GetEnumerator","opc.iopccertificateset_getenumerator"]
old-location: opc\iopccertificateset_getenumerator.htm
tech.root: OPC
ms.assetid: a48b9225-07cb-4367-b011-dc2297c2c4b3
ms.date: 12/05/2018
ms.keywords: GetEnumerator, GetEnumerator method [Open Packaging Conventions], GetEnumerator method [Open Packaging Conventions],IOpcCertificateSet interface, IOpcCertificateSet interface [Open Packaging Conventions],GetEnumerator method, IOpcCertificateSet.GetEnumerator, IOpcCertificateSet::GetEnumerator, msopc/IOpcCertificateSet::GetEnumerator, opc.iopccertificateset_getenumerator
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOpcCertificateSet::GetEnumerator
 - msopc/IOpcCertificateSet::GetEnumerator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcCertificateSet.GetEnumerator
---

# IOpcCertificateSet::GetEnumerator


## -description

Gets an enumerator of certificates in the set.

## -parameters

### -param certificateEnumerator [out, retval]

A pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator">IOpcCertificateEnumerator</a> interface of certificates in the set.

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

<a href="/windows/desktop/SecCrypto/certificates">Certificates</a>



<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset">IOpcCertificateSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>