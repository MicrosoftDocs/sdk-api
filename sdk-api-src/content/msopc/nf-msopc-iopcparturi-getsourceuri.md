---
UID: NF:msopc.IOpcPartUri.GetSourceUri
title: IOpcPartUri::GetSourceUri (msopc.h)
description: Gets the source URI of the relationships that are stored in a Relationships part. The current part URI object represents the part name of that Relationships part.
helpviewer_keywords: ["GetSourceUri","GetSourceUri method [Open Packaging Conventions]","GetSourceUri method [Open Packaging Conventions]","IOpcPartUri interface","IOpcPartUri interface [Open Packaging Conventions]","GetSourceUri method","IOpcPartUri.GetSourceUri","IOpcPartUri::GetSourceUri","msopc/IOpcPartUri::GetSourceUri","opc.iopcparturi_getsourceuri"]
old-location: opc\iopcparturi_getsourceuri.htm
tech.root: OPC
ms.assetid: 02e8570b-3826-4619-b4f5-c1f74e27aefc
ms.date: 12/05/2018
ms.keywords: GetSourceUri, GetSourceUri method [Open Packaging Conventions], GetSourceUri method [Open Packaging Conventions],IOpcPartUri interface, IOpcPartUri interface [Open Packaging Conventions],GetSourceUri method, IOpcPartUri.GetSourceUri, IOpcPartUri::GetSourceUri, msopc/IOpcPartUri::GetSourceUri, opc.iopcparturi_getsourceuri
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOpcPartUri::GetSourceUri
 - msopc/IOpcPartUri::GetSourceUri
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
 - IOpcPartUri.GetSourceUri
---

# IOpcPartUri::GetSourceUri


## -description

Gets  the source URI of the relationships that are stored in a  Relationships part. The  current part URI object represents the part name of that Relationships part.

## -parameters

### -param sourceUri [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcuri">IOpcUri</a> interface of the OPC URI object that represents the  URI of the source of the relationships stored in the Relationships part.

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
The <i>sourceUri</i> parameter is <b>NULL</b>.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_RELATIONSHIP_URI_REQUIRED</b></dt>
<dt>0x80510003</dt>
</dl>
</td>
<td width="60%">
The part name of a Relationships part is required, but the part name is not that of a Relationships part.

For more information about the part names of Relationships parts, see the <i>OPC</i>.

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

If the current part URI object represents the part name of the Relationships part that stores package relationships ("/_rels/.rels"),  the OPC URI object returned in <i>sourceUri</i> will represent the package root ("/").
        

If the current part URI object is not the part name of a Relationships part,  this method fails with the <b>OPC_E_RELATIONSHIP_URI_REQUIRED</b> error. The syntax for Relationship part names is specified in the <i>OPC</i>.

The following table shows possible current part URIs and the source URI that would be returned by this method. <table>
<tr>
<th>Current Part URI </th>
<th>Current Part URI Description</th>
<th>Source URI</th>
<th>Source URI Description</th>
<th>Return Value</th>
</tr>
<tr>
<td>/mydoc/_rels/picture.jpg.rels</td>
<td>The part name of a  Relationships part</td>
<td>/mydoc/picture.jpg</td>
<td>The part name of the part that is the source of the relationships stored in the Relationships part that is represented by the current part URI object</td>
<td><b>S_OK</b></td>
</tr>
<tr>
<td>/_rels/.rels</td>
<td>The part name of a  Relationships part</td>
<td>/</td>
<td>The package root; the source of the relationships stored in the Relationships part that is represented by the current part URI object</td>
<td><b>S_OK</b></td>
</tr>
<tr>
<td>/mydoc/image/chart1.jpg</td>
<td>The part name of a  part that is not a Relationships part</td>
<td>Undefined</td>
<td> Undefined</td>
<td><b>OPC_E_RELATIONSHIP_URI_REQUIRED</b></td>
</tr>
<tr>
<td>/_rels/a.jpg</td>
<td>The part name of a  part that is not a Relationships part</td>
<td>Undefined</td>
<td> Undefined</td>
<td><b>OPC_E_RELATIONSHIP_URI_REQUIRED</b></td>
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



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a>



<a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>



<b>Reference</b>