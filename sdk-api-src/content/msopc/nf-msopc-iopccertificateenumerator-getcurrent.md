---
UID: NF:msopc.IOpcCertificateEnumerator.GetCurrent
title: IOpcCertificateEnumerator::GetCurrent (msopc.h)
author: windows-sdk-content
description: Gets the CERT_CONTEXT structure at the current position of the enumerator.
old-location: opc\iopccertificateenumerator_getcurrent.htm
tech.root: OPC
ms.assetid: edd2afc1-cafd-4a52-b2df-1a1fcdf1d6fa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCurrent, GetCurrent method [Open Packaging Conventions], GetCurrent method [Open Packaging Conventions],IOpcCertificateEnumerator interface, IOpcCertificateEnumerator interface [Open Packaging Conventions],GetCurrent method, IOpcCertificateEnumerator.GetCurrent, IOpcCertificateEnumerator::GetCurrent, msopc/IOpcCertificateEnumerator::GetCurrent, opc.iopccertificateenumerator_getcurrent
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
 - IOpcCertificateEnumerator.GetCurrent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcCertificateEnumerator::GetCurrent


## -description


Gets the <a href="http://msdn.microsoft.com/en-us/library/aa377189(vs.85).aspx">CERT_CONTEXT</a> structure at the current position of the enumerator.
        


## -parameters




### -param certificate [out, retval]

A  pointer to a <a href="http://msdn.microsoft.com/en-us/library/aa377189(vs.85).aspx">CERT_CONTEXT</a> structure.
            If the method succeeds, call the <a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a> function to free the memory of the structure.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
            

<table>
<tr>
<th>Return code/value</th>
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
The <i>partReference</i> parameter is <b>NULL</b>.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_ENUM_COLLECTION_CHANGED</b></dt>
<dt>0x80510050</dt>
</dl>
</td>
<td width="60%">
The enumerator is invalid because the underlying set has changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_ENUM_INVALID_POSITION</b></dt>
<dt>0x80510053</dt>
</dl>
</td>
<td width="60%">
The enumerator cannot perform this operation from its current position.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_EXTERNAL_SIGNATURE</b></dt>
<dt>0x8051001E</dt>
</dl>
</td>
<td width="60%">
A relationship whose target is a  Signature part has the external target mode; Signature parts must be inside of the package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_INVALID_CERTIFICATE_RELATIONSHIP</b></dt>
<dt>0x8051001D</dt>
</dl>
</td>
<td width="60%">
A relationship of type  digital signature certificate has the external target mode.

For more information about this relationship type, see the <i>OPC</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_INVALID_RELATIONSHIP_TRANSFORM_XML</b></dt>
<dt>0x80510021</dt>
</dl>
</td>
<td width="60%">
A <b>Transform</b> element that indicates the use of the relationships transform and  the selection criteria for the transform does not conform to the schema specified in the <i>OPC</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_MISSING_CERTIFICATE_PART</b></dt>
<dt>0x80510056</dt>
</dl>
</td>
<td width="60%">
The part that contains the certificate and is the target of a relationship of type digital signature certificate does not exist.

For more information about this relationship type, see the <i>OPC</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_SIGNATURE_PROPERTY_MISSING_TARGET</b></dt>
<dt>0x80510045</dt>
</dl>
</td>
<td width="60%">
The <b>SignatureProperty</b> element is missing the required <b>Target</b> attribute.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_UNEXPECTED_CONTENT_TYPE</b></dt>
<dt>0x80510005</dt>
</dl>
</td>
<td width="60%">
Either the content type of a part differed from the expected content type (specified in the OPC, <a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 Part 2</a>), or the part content did not match the part's  content type.

</td>
</tr>
</table>
 




## -remarks



If the certificate represented by the <a href="http://msdn.microsoft.com/en-us/library/aa377189(vs.85).aspx">CERT_CONTEXT</a> structure is corrupted or is not an X.509 certificate, this method will return an error; further,  the signing policy used by the caller dictates whether the signature will still be validated. After this kind of error is returned, calls to the <a href="https://msdn.microsoft.com/81918b97-0d10-4d7c-aaad-fc886d55e664">MoveNext</a> or <a href="https://msdn.microsoft.com/564c391c-8c73-4dd8-b713-3a5309708fd6">MovePrevious</a> method will continue to iterate through the enumerator.

When an enumerator is created, the current position precedes the first pointer of the enumerator. To set the current position to the first pointer, call the  <a href="https://msdn.microsoft.com/81918b97-0d10-4d7c-aaad-fc886d55e664">MoveNext</a>method after the enumerator is created.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376489(v=VS.85).aspx">Certificates</a>



<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/a66ad728-9d20-44d9-a363-1d2a7927d810">IOpcCertificateEnumerator</a>



<a href="https://msdn.microsoft.com/0ac56b41-a120-4a9b-9bfa-afba1ba0f3b4">IOpcCertificateSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

