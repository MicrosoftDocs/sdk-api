---
UID: NF:msopc.IOpcDigitalSignature.GetCustomReferenceEnumerator
title: IOpcDigitalSignature::GetCustomReferenceEnumerator (msopc.h)
author: windows-sdk-content
description: Gets an enumerator of the IOpcSignatureReference interface pointers that represent references to application-specific XML elements that have been signed.
old-location: opc\iopcdigitalsignature_getcustomreferenceenumerator.htm
tech.root: OPC
ms.assetid: 8cc5ae5d-faef-451d-8ad8-db4b8b5c0e22
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCustomReferenceEnumerator, GetCustomReferenceEnumerator method [Open Packaging Conventions], GetCustomReferenceEnumerator method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetCustomReferenceEnumerator method, IOpcDigitalSignature.GetCustomReferenceEnumerator, IOpcDigitalSignature::GetCustomReferenceEnumerator, msopc/IOpcDigitalSignature::GetCustomReferenceEnumerator, opc.iopcdigitalsignature_getcustomreferenceenumerator
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
 - IOpcDigitalSignature.GetCustomReferenceEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcDigitalSignature::GetCustomReferenceEnumerator


## -description


Gets an enumerator of the <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointers that represent references to application-specific XML elements that have been signed.


## -parameters




### -param customReferenceEnumerator [out, retval]

A pointer to an enumerator of <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointers.  An <b>IOpcSignatureReference</b> interface pointer represents a reference to an application-specific XML element that has been signed.


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
The <i>customReferenceEnumerator</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



To access the signed XML Element by using an <a href="https://msdn.microsoft.com/4ebb4fbe-66cc-46d9-b548-31177d9f6da9">IOpcSignatureCustomObject</a> interface pointer, call the <a href="https://msdn.microsoft.com/a0197da5-e613-4aba-8098-901e192051ff">IOpcSignatureCustomObjectEnumerator::GetCurrent</a> method. To access the markup of the signed XML element, call the <a href="https://msdn.microsoft.com/fedb6f47-59b9-4959-91ef-db1fb398aca9">IOpcSignatureCustomObject::GetXml</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/e82caa1e-4cf8-457f-86d9-24f707544199">IOpcSignatureCustomObjectEnumerator</a>



<a href="https://msdn.microsoft.com/1d0a14c6-826c-419f-9e94-d5929fdbae82">IOpcSignatureReferenceEnumerator</a>



<a href="https://msdn.microsoft.com/7955ac86-de6e-4911-a107-a1617c14e685">IOpcSignatureReferenceSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

