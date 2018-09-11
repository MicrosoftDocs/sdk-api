---
UID: NF:msopc.IOpcFactory.CreatePartUri
title: IOpcFactory::CreatePartUri
author: windows-sdk-content
description: Creates a part URI object that represents a part name.
old-location: opc\iopcfactory_createparturi.htm
tech.root: OPC
ms.assetid: 8634d166-767a-46a5-9001-5fca88bfa844
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreatePartUri, CreatePartUri method [Open Packaging Conventions], CreatePartUri method [Open Packaging Conventions],IOpcFactory interface, IOpcFactory interface [Open Packaging Conventions],CreatePartUri method, IOpcFactory.CreatePartUri, IOpcFactory::CreatePartUri, msopc/IOpcFactory::CreatePartUri, opc.iopcfactory_createparturi
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IOpcFactory.CreatePartUri
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcFactory::CreatePartUri


## -description


Creates a part URI object that represents a part name.


## -parameters




### -param pwzUri [in]

A  URI that represents the location of a part relative to the root of the package that contains it.


### -param partUri [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface of the part URI object. This object represents the  part name derived from the URI passed in <i>pwzUri</i>.

Part names must conform to the syntax specified in the <i>OPC</i>.


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
At least one of the  <i>pwzUri</i> and <i>partUri</i> parameters is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_NONCONFORMING_URI</b></dt>
<dt>0x80510001</dt>
</dl>
</td>
<td width="60%">
A part name cannot be the empty string "".

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_NONCONFORMING_URI</b></dt>
<dt>0x80510001</dt>
</dl>
</td>
<td width="60%">
A part name cannot be a '/'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_NONCONFORMING_URI</b></dt>
<dt>0x80510001</dt>
</dl>
</td>
<td width="60%">
A part name cannot begin with  "//".

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_NONCONFORMING_URI</b></dt>
<dt>0x80510001</dt>
</dl>
</td>
<td width="60%">
A part name cannot end with a '/'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_NONCONFORMING_URI</b></dt>
<dt>0x80510001</dt>
</dl>
</td>
<td width="60%">
A part name cannot end with a '.'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_NONCONFORMING_URI</b></dt>
<dt>0x80510001</dt>
</dl>
</td>
<td width="60%">
A part name cannot have any segments that end with a '.'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_NONCONFORMING_URI</b></dt>
<dt>0x80510001</dt>
</dl>
</td>
<td width="60%">
A part name cannot have fragment component. A fragment component is preceded by a '#' character, as described in <a href="http://go.microsoft.com/fwlink/p/?linkid=143950">RFC 3986: URI Generic Syntax</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_NONCONFORMING_URI</b></dt>
<dt>0x80510001</dt>
</dl>
</td>
<td width="60%">
A part name cannot be the name of a Relationships part that indicates another Relationships part as the source of the relationships contained therein.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_RELATIVE_URI_REQUIRED</b></dt>
<dt>0x80510002</dt>
</dl>
</td>
<td width="60%">
A part name cannot be an absolute URI. An absolute URI begins with a schema component followed by a ":", as described in <a href="http://go.microsoft.com/fwlink/p/?linkid=143950">RFC 3986: URI Generic Syntax</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>CreateUri</b> function error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="https://msdn.microsoft.com/library/ms775098(v=VS.85).aspx">CreateUri</a> function. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WinINet error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from a  <a href="https://msdn.microsoft.com/dd2f8246-ea82-49cb-973f-157fb77c8c08">WinINet</a> API. 

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




<a href="https://msdn.microsoft.com/library/ms775098(v=VS.85).aspx">CreateUri</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/0a265a0a-c109-4afc-a0ad-d3ee31757aa1">IOpcFactory</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="https://msdn.microsoft.com/95da581d-3d30-4cd7-bd20-f44bf505ac0a">Parts Overview</a>



<a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=143950">RFC 3986: URI Generic Syntax</a>



<b>Reference</b>
 

 

