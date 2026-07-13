---
UID: NF:msopc.IOpcUri.GetRelativeUri
title: IOpcUri::GetRelativeUri (msopc.h)
description: Forms a relative URI for a specified part, relative to the URI represented by the current OPC URI object.
helpviewer_keywords: ["GetRelativeUri","GetRelativeUri method [Open Packaging Conventions]","GetRelativeUri method [Open Packaging Conventions]","IOpcUri interface","IOpcUri interface [Open Packaging Conventions]","GetRelativeUri method","IOpcUri.GetRelativeUri","IOpcUri::GetRelativeUri","msopc/IOpcUri::GetRelativeUri","opc.iopcuri_getrelativeuri"]
old-location: opc\iopcuri_getrelativeuri.htm
tech.root: OPC
ms.assetid: ce98b0a6-f4b3-4f49-897a-f144af7dfc49
ms.date: 12/05/2018
ms.keywords: GetRelativeUri, GetRelativeUri method [Open Packaging Conventions], GetRelativeUri method [Open Packaging Conventions],IOpcUri interface, IOpcUri interface [Open Packaging Conventions],GetRelativeUri method, IOpcUri.GetRelativeUri, IOpcUri::GetRelativeUri, msopc/IOpcUri::GetRelativeUri, opc.iopcuri_getrelativeuri
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
 - IOpcUri::GetRelativeUri
 - msopc/IOpcUri::GetRelativeUri
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
 - IOpcUri.GetRelativeUri
---

# IOpcUri::GetRelativeUri


## -description

 Forms a relative URI for a specified part, relative to the URI represented by the current OPC URI object.

## -parameters

### -param targetPartUri [in]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface of the part URI object that represents the part name from which the relative URI is formed.

### -param relativeUri [out, retval]

A pointer to the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775038(v=vs.85)">IUri</a> interface of the URI of the part, relative to the current OPC URI object.

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
 At least one of the <i>targetPartUri</i>, and <i>relativePartUri</i> parameters is <b>NULL</b>.

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

Example input and output:


<table>
<tr>
<th>Input <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> represents</th>
<th>Current <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcuri">IOpcUri</a> represents</th>
<th>Returned relative <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775038(v=vs.85)">IUri</a> represents</th>
</tr>
<tr>
<td>/mydoc/markup/page.xml</td>
<td>	/mydoc/markup/picture.jpg	</td>
<td>picture.jpg</td>
</tr>
<tr>
<td>/mydoc/markup/page.xml</td>
<td>/mydoc/picture.jpg</td>
<td>../picture.jpg</td>
</tr>
<tr>
<td>/mydoc/markup/page.xml</td>
<td>/mydoc/images/pictures.jpg</td>
<td>../images/pictures.jpg</td>
</tr>
</table>
 



<h3><a id="Support_on__Previous_Windows_Versions"></a><a id="support_on__previous_windows_versions"></a><a id="SUPPORT_ON__PREVIOUS_WINDOWS_VERSIONS"></a>Support on  Previous Windows Versions</h3>
The behavior and performance of this method is the same on all supported Windows versions. For more information, see <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>, and <a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcuri">IOpcUri</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>



<b>Reference</b>