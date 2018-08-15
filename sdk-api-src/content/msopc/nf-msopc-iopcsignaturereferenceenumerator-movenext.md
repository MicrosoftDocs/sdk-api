---
UID: NF:msopc.IOpcSignatureReferenceEnumerator.MoveNext
title: IOpcSignatureReferenceEnumerator::MoveNext
author: windows-sdk-content
description: Moves the current position of the enumerator to the next IOpcSignatureReference interface pointer.
old-location: opc\iopcsignaturereferenceenumerator_movenext.htm
old-project: OPC
ms.assetid: b7a260c3-cfe5-4dcb-9628-7cf7fdf382de
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IOpcSignatureReferenceEnumerator interface [Open Packaging Conventions],MoveNext method, IOpcSignatureReferenceEnumerator.MoveNext, IOpcSignatureReferenceEnumerator::MoveNext, MoveNext, MoveNext method [Open Packaging Conventions], MoveNext method [Open Packaging Conventions],IOpcSignatureReferenceEnumerator interface, msopc/IOpcSignatureReferenceEnumerator::MoveNext, opc.iopcsignaturereferenceenumerator_movenext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msopc.h
req.include-header: 
req.redist: 
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
 - IOpcSignatureReferenceEnumerator.MoveNext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcSignatureReferenceEnumerator::MoveNext


## -description


Moves the current position of the enumerator to the next <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointer.


## -parameters




### -param hasNext [out, retval]

A Boolean value that indicates the status of the <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointer at the current position.

The value of <i>hasNext</i> is only valid when the method succeeds.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>TRUE</dt>
</dl>
</td>
<td width="60%">
The current position of the enumerator has been advanced to the next pointer and that pointer is valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>FALSE</dt>
</dl>
</td>
<td width="60%">
The current position of the enumerator has been advanced past the end of the collection and is no longer valid.

</td>
</tr>
</table>
 


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
The <i>hasNext</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_ENUM_CANNOT_MOVE_NEXT</b></dt>
<dt>0x80510051</dt>
</dl>
</td>
<td width="60%">
The current position is already past the last item of the enumerator.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/1d0a14c6-826c-419f-9e94-d5929fdbae82">IOpcSignatureReferenceEnumerator</a>



<a href="https://msdn.microsoft.com/7955ac86-de6e-4911-a107-a1617c14e685">IOpcSignatureReferenceSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

