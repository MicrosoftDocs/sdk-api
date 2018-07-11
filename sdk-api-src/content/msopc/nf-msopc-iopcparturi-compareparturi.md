---
UID: NF:msopc.IOpcPartUri.ComparePartUri
title: IOpcPartUri::ComparePartUri
author: windows-sdk-content
description: Returns an integer that indicates whether the URIs represented by the current part URI object and a specified part URI object are equivalent.
old-location: opc\iopcparturi_compareparturi.htm
old-project: OPC
ms.assetid: b97890f8-dc9d-494f-82f9-3d32c09f5d67
ms.author: windowssdkdev
ms.date: 03/15/2018
ms.keywords: ComparePartUri, ComparePartUri method [Open Packaging Conventions], ComparePartUri method [Open Packaging Conventions],IOpcPartUri interface, IOpcPartUri interface [Open Packaging Conventions],ComparePartUri method, IOpcPartUri.ComparePartUri, IOpcPartUri::ComparePartUri, msopc/IOpcPartUri::ComparePartUri, opc.iopcparturi_compareparturi
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Opcparturi.idl
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
 - IOpcPartUri.ComparePartUri
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcPartUri::ComparePartUri


## -description


Returns an integer that indicates whether the URIs represented by the current part URI object and a specified part URI object are equivalent.


## -parameters




### -param partUri [in]

A pointer to the <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface of the part URI object to compare with the current part URI object.


### -param comparisonResult [out, retval]

Receives an integer that indicates whether the two part URI objects are equivalent.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>&lt;0</dt>
</dl>
</td>
<td width="60%">
The current part URI object is less than the input part URI object that is passed in <i>partUri</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The current part URI object is equivalent to the input part URI object that is passed in <i>partUri</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>&gt;0</dt>
</dl>
</td>
<td width="60%">
The current part URI object is greater than the input part URI object that is passed in <i>partUri</i>.

</td>
</tr>
</table>
 


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
 At least one of the <i>partUri</i>, and <i>comparisonResult</i> parameters is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Support_on__Previous_Windows_Versions"></a><a id="support_on__previous_windows_versions"></a><a id="SUPPORT_ON__PREVIOUS_WINDOWS_VERSIONS"></a>Support on  Previous Windows Versions</h3>
The behavior and performance of this method is the same on all supported Windows versions. For more information, see <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>, and <a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/95da581d-3d30-4cd7-bd20-f44bf505ac0a">Parts Overview</a>



<a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>



<b>Reference</b>
 

 

