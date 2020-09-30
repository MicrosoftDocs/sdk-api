---
UID: NF:msopc.IOpcPartUri.IsRelationshipsPartUri
title: IOpcPartUri::IsRelationshipsPartUri (msopc.h)
description: Returns a value that indicates whether the current part URI object represents the part name of a Relationships part.
helpviewer_keywords: ["IOpcPartUri interface [Open Packaging Conventions]","IsRelationshipsPartUri method","IOpcPartUri.IsRelationshipsPartUri","IOpcPartUri::IsRelationshipsPartUri","IsRelationshipsPartUri","IsRelationshipsPartUri method [Open Packaging Conventions]","IsRelationshipsPartUri method [Open Packaging Conventions]","IOpcPartUri interface","msopc/IOpcPartUri::IsRelationshipsPartUri","opc.iopcparturi_isrelationshipsparturi"]
old-location: opc\iopcparturi_isrelationshipsparturi.htm
tech.root: OPC
ms.assetid: 11d271ab-247c-4060-b769-45e462b66255
ms.date: 12/05/2018
ms.keywords: IOpcPartUri interface [Open Packaging Conventions],IsRelationshipsPartUri method, IOpcPartUri.IsRelationshipsPartUri, IOpcPartUri::IsRelationshipsPartUri, IsRelationshipsPartUri, IsRelationshipsPartUri method [Open Packaging Conventions], IsRelationshipsPartUri method [Open Packaging Conventions],IOpcPartUri interface, msopc/IOpcPartUri::IsRelationshipsPartUri, opc.iopcparturi_isrelationshipsparturi
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
 - IOpcPartUri::IsRelationshipsPartUri
 - msopc/IOpcPartUri::IsRelationshipsPartUri
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
 - IOpcPartUri.IsRelationshipsPartUri
---

# IOpcPartUri::IsRelationshipsPartUri


## -description

Returns a value that indicates whether the current part URI object represents the part name of a Relationships part.

## -parameters

### -param isRelationshipUri [out, retval]

Receives a value that indicates whether the current part URI object represents the part name of a Relationships part.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The current part URI object represents the part name of a Relationships part.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The current part URI object does not represent the part name of a Relationships part.

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
The <i>isRelationshipUri</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

<h3><a id="Support_on__Previous_Windows_Versions"></a><a id="support_on__previous_windows_versions"></a><a id="SUPPORT_ON__PREVIOUS_WINDOWS_VERSIONS"></a>Support on  Previous Windows Versions</h3>
The behavior and performance of this method is the same on all supported Windows versions. For more information, see <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>, and <a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>



<b>Reference</b>