---
UID: NF:msopc.IOpcSignatureReference.GetUri
title: IOpcSignatureReference::GetUri
author: windows-sdk-content
description: Gets the URI of the referenced XML element.
old-location: opc\iopcsignaturereference_geturi.htm
old-project: OPC
ms.assetid: 4dd02f48-9b49-4e74-b0cf-c51c0a594437
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetUri, GetUri method [Open Packaging Conventions], GetUri method [Open Packaging Conventions],IOpcSignatureReference interface, IOpcSignatureReference interface [Open Packaging Conventions],GetUri method, IOpcSignatureReference.GetUri, IOpcSignatureReference::GetUri, msopc/IOpcSignatureReference::GetUri, opc.iopcsignaturereference_geturi
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcSignatureReference.GetUri
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcSignatureReference::GetUri


## -description


Gets the URI of the referenced XML element.


## -parameters




### -param referenceUri [out, retval]

A pointer to the  URI of the referenced element.

This URI represented by a string is  "#" followed by  the <b>Id</b> attribute value of the referenced element: "#<i>&lt;elementIdValue&gt;</i>".

For examples, see the Remarks section.


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
The <i>referenceUri</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The URI of the referenced element is serialized in the signature markup as the <b>URI</b> attribute of a <b>Reference</b> element.

The following table shows two examples of the <i>referenceUri</i> parameter value represented as strings.<table>
<tr>
<th><i>referenceUri</i> Value as String</th>
<th>Referenced Element</th>
<th>Element Description</th>
</tr>
<tr>
<td>"#<i>idMyCustomObject</i>"</td>
<td>"&lt;Object Id="<i>idMyCustomObject</i>"&gt;<i>...</i>&lt;/Object&gt;"</td>
<td>
An application-specific <b>Object</b> element.

</td>
</tr>
<tr>
<td>"#<i>idMyElement</i>"</td>
<td>"&lt;Object&gt;&lt;<i>MyElement</i> Id="<i>idMyElement</i>"&gt;<i>...</i>&lt;/<i>MyElement</i>&gt;...&lt;/Object&gt;"</td>
<td>
A child element of an application-specific <b>Object</b>.

</td>
</tr>
</table>
 




#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

