---
UID: NF:msopc.IOpcUri.GetRelationshipsPartUri
title: IOpcUri::GetRelationshipsPartUri
author: windows-sdk-content
description: Gets the part name of the Relationships part that stores relationships that have the source URI represented by the current OPC URI object.
old-location: opc\iopcuri_getrelationshipsparturi.htm
tech.root: OPC
ms.assetid: 1b953b4c-6e8d-4097-a6bf-618b49cdd603
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRelationshipsPartUri, GetRelationshipsPartUri method [Open Packaging Conventions], GetRelationshipsPartUri method [Open Packaging Conventions],IOpcUri interface, IOpcUri interface [Open Packaging Conventions],GetRelationshipsPartUri method, IOpcUri.GetRelationshipsPartUri, IOpcUri::GetRelationshipsPartUri, msopc/IOpcUri::GetRelationshipsPartUri, opc.iopcuri_getrelationshipsparturi
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Opcparturi.idl
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
 - IOpcUri.GetRelationshipsPartUri
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcUri::GetRelationshipsPartUri


## -description


Gets the part name of the Relationships part that stores relationships that have the source URI represented by the  current OPC URI object.


## -parameters




### -param relationshipPartUri [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface of the part URI object that represents the part name of the Relationships part. The source URI of the relationships stored in this Relationships part is represented by the  current OPC URI object.


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
The <i>relationshipPartUri</i> parameter is <b>NULL</b>.
              

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
The current <a href="https://msdn.microsoft.com/35ce7946-f7e7-4ac3-852f-e3fcca23d6d4">IOpcUri</a> represents a Relationships part and cannot be the source of any relationships.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>CreateUri</b> function error
              </b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="inet_CreateUri_Function">CreateUri</a> function.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WinINet error
              </b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from a  <a href="https://msdn.microsoft.com/dd2f8246-ea82-49cb-973f-157fb77c8c08">WinINet</a> API.
              

</td>
</tr>
</table>
 




## -remarks



The following table shows Relationships part URIs for some OPC URIs.<table>
<tr>
<th>OPC URI</th>
<th>Relationships Part Name</th>
<th> Return Value</th>
</tr>
<tr>
<td>/mydoc/images/picture.jpg</td>
<td>/mydoc/images/_rels/picture.jpg.rels</td>
<td><b>S_OK</b></td>
</tr>
<tr>
<td>/</td>
<td>/_rels/.rels</td>
<td><b>S_OK</b></td>
</tr>
<tr>
<td>/mydoc/images/_rels/picture.jpg.rels</td>
<td>Undefined</td>
<td><b>OPC_E_NONCONFORMING_URI</b></td>
</tr>
</table>
 



<h3><a id="Support_on__Previous_Windows_Versions"></a><a id="support_on__previous_windows_versions"></a><a id="SUPPORT_ON__PREVIOUS_WINDOWS_VERSIONS"></a>Support on  Previous Windows Versions</h3>
The behavior and performance of this method is the same on all supported Windows versions. For more information, see <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>, and <a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/35ce7946-f7e7-4ac3-852f-e3fcca23d6d4">IOpcUri</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>



<b>Reference</b>
 

 

