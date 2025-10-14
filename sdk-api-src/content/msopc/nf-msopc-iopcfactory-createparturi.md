---
UID: NF:msopc.IOpcFactory.CreatePartUri
title: IOpcFactory::CreatePartUri (msopc.h)
description: Creates a part URI object that represents a part name.
helpviewer_keywords: ["CreatePartUri","CreatePartUri method [Open Packaging Conventions]","CreatePartUri method [Open Packaging Conventions]","IOpcFactory interface","IOpcFactory interface [Open Packaging Conventions]","CreatePartUri method","IOpcFactory.CreatePartUri","IOpcFactory::CreatePartUri","msopc/IOpcFactory::CreatePartUri","opc.iopcfactory_createparturi"]
old-location: opc\iopcfactory_createparturi.htm
tech.root: OPC
ms.assetid: 8634d166-767a-46a5-9001-5fca88bfa844
ms.date: 12/05/2018
ms.keywords: CreatePartUri, CreatePartUri method [Open Packaging Conventions], CreatePartUri method [Open Packaging Conventions],IOpcFactory interface, IOpcFactory interface [Open Packaging Conventions],CreatePartUri method, IOpcFactory.CreatePartUri, IOpcFactory::CreatePartUri, msopc/IOpcFactory::CreatePartUri, opc.iopcfactory_createparturi
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOpcFactory::CreatePartUri
 - msopc/IOpcFactory::CreatePartUri
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
 - IOpcFactory.CreatePartUri
---

# IOpcFactory::CreatePartUri


## -description

Creates a part URI object that represents a part name.

## -parameters

### -param pwzUri [in]

A  URI that represents the location of a part relative to the root of the package that contains it.

### -param partUri [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface of the part URI object. This object represents the  part name derived from the URI passed in <i>pwzUri</i>.

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
A part name cannot have fragment component. A fragment component is preceded by a '#' character, as described in <a href="https://www.ietf.org/rfc/rfc3986.txt">RFC 3986: URI Generic Syntax</a>.

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
A part name cannot be an absolute URI. An absolute URI begins with a schema component followed by a ":", as described in <a href="https://www.ietf.org/rfc/rfc3986.txt">RFC 3986: URI Generic Syntax</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CreateUri function error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775098(v=vs.85)">CreateUri</a> function. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WinINet error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from a  <a href="/windows/desktop/WinInet/wininet-reference">WinINet</a> API. 

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

<a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775098(v=vs.85)">CreateUri</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory">IOpcFactory</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a>



<a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>



<a href="https://www.ietf.org/rfc/rfc3986.txt">RFC 3986: URI Generic Syntax</a>



<b>Reference</b>