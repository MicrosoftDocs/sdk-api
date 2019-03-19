---
UID: NF:msopc.IOpcSignaturePartReference.GetDigestMethod
title: IOpcSignaturePartReference::GetDigestMethod (msopc.h)
author: windows-sdk-content
description: Gets the digest method to use on part content of the referenced part when the part is signed.
old-location: opc\iopcsignaturepartreference_getdigestmethod.htm
tech.root: OPC
ms.assetid: 750aec1a-92b4-4c70-8c17-c15c9536bc41
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDigestMethod, GetDigestMethod method [Open Packaging Conventions], GetDigestMethod method [Open Packaging Conventions],IOpcSignaturePartReference interface, IOpcSignaturePartReference interface [Open Packaging Conventions],GetDigestMethod method, IOpcSignaturePartReference.GetDigestMethod, IOpcSignaturePartReference::GetDigestMethod, msopc/IOpcSignaturePartReference::GetDigestMethod, opc.iopcsignaturepartreference_getdigestmethod
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
 - IOpcSignaturePartReference.GetDigestMethod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcSignaturePartReference::GetDigestMethod


## -description


Gets the digest method to use on part content of the referenced part when the part is signed.


## -parameters




### -param digestMethod [out, retval]

The digest method to use on part content of the referenced part when the part is signed.


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
The <i>digestMethod</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method allocates memory used by the string returned in <i>digestMethod</i>.  If the method succeeds, call the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function to free the memory.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

