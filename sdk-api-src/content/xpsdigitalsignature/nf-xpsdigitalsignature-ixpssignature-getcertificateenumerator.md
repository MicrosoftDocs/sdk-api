---
UID: NF:xpsdigitalsignature.IXpsSignature.GetCertificateEnumerator
title: IXpsSignature::GetCertificateEnumerator (xpsdigitalsignature.h)
author: windows-sdk-content
description: Gets a pointer to an IOpcCertificateEnumerator interface, which enumerates the package certificates that are attached to the signature.
old-location: xps\ixpssignature_getcertificateenumerator.htm
tech.root: printdocs
ms.assetid: e4af0aa3-8420-4297-993c-dda4d4f7cf61
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCertificateEnumerator, GetCertificateEnumerator method [XPS Documents and Packaging], GetCertificateEnumerator method [XPS Documents and Packaging],IXpsSignature interface, IXpsSignature interface [XPS Documents and Packaging],GetCertificateEnumerator method, IXpsSignature.GetCertificateEnumerator, IXpsSignature::GetCertificateEnumerator, xps.ixpssignature_getcertificateenumerator, xpsdigitalsignature/IXpsSignature::GetCertificateEnumerator
ms.topic: method
req.header: xpsdigitalsignature.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsDigitalSignature.idl
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
 - xpsdigitalsignature.h
api_name:
 - IXpsSignature.GetCertificateEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSignature::GetCertificateEnumerator


## -description


Gets a pointer to an <a href="https://msdn.microsoft.com/a66ad728-9d20-44d9-a363-1d2a7927d810">IOpcCertificateEnumerator</a> interface, which enumerates the package certificates that are attached to the signature.


## -parameters




### -param certificateEnumerator [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/a66ad728-9d20-44d9-a363-1d2a7927d810">IOpcCertificateEnumerator</a> interface, which enumerates the certificates that are attached to the signature.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For return values that are not listed in this table, see <a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a> and  <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The interface is not connected to the signature manager.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/a66ad728-9d20-44d9-a363-1d2a7927d810">IOpcCertificateEnumerator</a> interface returned in <i>certificateEnumerator</i> can be empty; however the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a> requires that at least the signing certificate be included in the XPS package. Package producers may include additional certificates as well. For example, the entire certificate trust chain could be included in the XPS package.




## -see-also




<a href="https://msdn.microsoft.com/a66ad728-9d20-44d9-a363-1d2a7927d810">IOpcCertificateEnumerator</a>



<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a>



<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

