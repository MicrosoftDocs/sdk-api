---
UID: NF:msopc.IOpcUri.GetRelationshipsPartUri
title: IOpcUri::GetRelationshipsPartUri (msopc.h)
description: Gets the part name of the Relationships part that stores relationships that have the source URI represented by the current OPC URI object.
helpviewer_keywords: ["GetRelationshipsPartUri","GetRelationshipsPartUri method [Open Packaging Conventions]","GetRelationshipsPartUri method [Open Packaging Conventions]","IOpcUri interface","IOpcUri interface [Open Packaging Conventions]","GetRelationshipsPartUri method","IOpcUri.GetRelationshipsPartUri","IOpcUri::GetRelationshipsPartUri","msopc/IOpcUri::GetRelationshipsPartUri","opc.iopcuri_getrelationshipsparturi"]
old-location: opc\iopcuri_getrelationshipsparturi.htm
tech.root: OPC
ms.assetid: 1b953b4c-6e8d-4097-a6bf-618b49cdd603
ms.date: 12/05/2018
ms.keywords: GetRelationshipsPartUri, GetRelationshipsPartUri method [Open Packaging Conventions], GetRelationshipsPartUri method [Open Packaging Conventions],IOpcUri interface, IOpcUri interface [Open Packaging Conventions],GetRelationshipsPartUri method, IOpcUri.GetRelationshipsPartUri, IOpcUri::GetRelationshipsPartUri, msopc/IOpcUri::GetRelationshipsPartUri, opc.iopcuri_getrelationshipsparturi
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOpcUri::GetRelationshipsPartUri
 - msopc/IOpcUri::GetRelationshipsPartUri
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
 - IOpcUri.GetRelationshipsPartUri
---

# IOpcUri::GetRelationshipsPartUri


## -description

Gets the part name of the Relationships part that stores relationships that have the source URI represented by the  current OPC URI object.

## -parameters

### -param relationshipPartUri [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface of the part URI object that represents the part name of the Relationships part. The source URI of the relationships stored in this Relationships part is represented by the  current OPC URI object.

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
The current <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcuri">IOpcUri</a> represents a Relationships part and cannot be the source of any relationships.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CreateUri function error
              </b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775098(v=vs.85)">CreateUri</a> function.
              

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
An <b>HRESULT</b> error code from a  <a href="/windows/desktop/WinInet/wininet-reference">WinINet</a> API.
              

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
The behavior and performance of this method is the same on all supported Windows versions. For more information, see <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>, and <a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcuri">IOpcUri</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>



<b>Reference</b>