---
UID: NF:msopc.IOpcPartUri.ComparePartUri
title: IOpcPartUri::ComparePartUri (msopc.h)
description: Returns an integer that indicates whether the URIs represented by the current part URI object and a specified part URI object are equivalent.
helpviewer_keywords: ["ComparePartUri","ComparePartUri method [Open Packaging Conventions]","ComparePartUri method [Open Packaging Conventions]","IOpcPartUri interface","IOpcPartUri interface [Open Packaging Conventions]","ComparePartUri method","IOpcPartUri.ComparePartUri","IOpcPartUri::ComparePartUri","msopc/IOpcPartUri::ComparePartUri","opc.iopcparturi_compareparturi"]
old-location: opc\iopcparturi_compareparturi.htm
tech.root: OPC
ms.assetid: b97890f8-dc9d-494f-82f9-3d32c09f5d67
ms.date: 12/05/2018
ms.keywords: ComparePartUri, ComparePartUri method [Open Packaging Conventions], ComparePartUri method [Open Packaging Conventions],IOpcPartUri interface, IOpcPartUri interface [Open Packaging Conventions],ComparePartUri method, IOpcPartUri.ComparePartUri, IOpcPartUri::ComparePartUri, msopc/IOpcPartUri::ComparePartUri, opc.iopcparturi_compareparturi
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
 - IOpcPartUri::ComparePartUri
 - msopc/IOpcPartUri::ComparePartUri
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
 - IOpcPartUri.ComparePartUri
---

# IOpcPartUri::ComparePartUri


## -description

Returns an integer that indicates whether the URIs represented by the current part URI object and a specified part URI object are equivalent.

## -parameters

### -param partUri [in]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface of the part URI object to compare with the current part URI object.

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



<a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a>



<a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>



<b>Reference</b>