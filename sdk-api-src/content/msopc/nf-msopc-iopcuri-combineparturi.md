---
UID: NF:msopc.IOpcUri.CombinePartUri
title: IOpcUri::CombinePartUri (msopc.h)
description: Forms the part name of the part that is referenced by the specified relative URI.
helpviewer_keywords: ["CombinePartUri","CombinePartUri method [Open Packaging Conventions]","CombinePartUri method [Open Packaging Conventions]","IOpcUri interface","IOpcUri interface [Open Packaging Conventions]","CombinePartUri method","IOpcUri.CombinePartUri","IOpcUri::CombinePartUri","msopc/IOpcUri::CombinePartUri","opc.iopcuri_combineparturi"]
old-location: opc\iopcuri_combineparturi.htm
tech.root: OPC
ms.assetid: 9bb4c351-12ef-4e26-bcb1-59f81a413588
ms.date: 12/05/2018
ms.keywords: CombinePartUri, CombinePartUri method [Open Packaging Conventions], CombinePartUri method [Open Packaging Conventions],IOpcUri interface, IOpcUri interface [Open Packaging Conventions],CombinePartUri method, IOpcUri.CombinePartUri, IOpcUri::CombinePartUri, msopc/IOpcUri::CombinePartUri, opc.iopcuri_combineparturi
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IOpcUri::CombinePartUri
 - msopc/IOpcUri::CombinePartUri
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
 - IOpcUri.CombinePartUri
---

# IOpcUri::CombinePartUri


## -description

Forms the part name of the part that is referenced by the specified relative URI.
        The specified relative URI of the part is resolved against the URI represented as the current OPC URI object.

## -parameters

### -param relativeUri [in]

A pointer to the  <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775038(v=vs.85)">IUri</a> interface of the relative URI of the part.

To form the part URI object that represents the part name, this input URI is resolved against the URI represented as the current OPC URI object. Therefore, the input URI must be relative to the URI represented by the current OPC URI object.

This URI may include a fragment component; however, the fragment will be ignored and will not be included in the part name to be formed. A fragment component is preceded by a '#', as described in <a href="https://www.ietf.org/rfc/rfc3986.txt">RFC 3986: URI Generic Syntax</a>.

### -param combinedUri [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface of the part URI object that represents the part name.
            

The part URI object is formed by resolving the relative URI in <i>relativeUri</i> against the URI represented by the current OPC URI object.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775085(v=vs.85)">CoInternetCombineUrl</a> function returned an invalid size.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the <i>relativeUri</i>, and <i>combinedUri</i> parameters is <b>NULL</b>.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The size of the buffer required by the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775085(v=vs.85)">CoInternetCombineUrl</a> function changed unexpectedly.
              

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
The part name does not conform to the rules specified in the <i>OPC</i> standards.
                

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
<dt><b>CoInternetCombineUrl function error
              </b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775085(v=vs.85)">CoInternetCombineUrl</a> function.
              

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

Example input and output:


<table>
<tr>
<th>Input relative <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775038(v=vs.85)">IUri</a></th>
<th>Current <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcuri">IOpcUri</a>
</th>
<th>Formed <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>
</th>
</tr>
<tr>
<td>picture.jpg</td>
<td>/mydoc/markup/page.xml</td>
<td>/mydoc/markup/picture.jpg</td>
</tr>
<tr>
<td>../picture.jpg</td>
<td>/mydoc/markup/page.xml</td>
<td>/mydoc/picture.jpg</td>
</tr>
<tr>
<td>../../images/picture.jpg</td>
<td>/mydoc/page.xml</td>
<td>/images/picture.jpg</td>
</tr>
</table>
 



For information about how to use this method to help resolve a part name, see <a href="/previous-versions/windows/desktop/opc/resolving-a-part-name-from-a-relationship-s-target-uri">Resolving a Part Name from a Target URI</a>.

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



<a href="https://www.ietf.org/rfc/rfc3986.txt">RFC 3986: URI Generic Syntax</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/resolving-a-part-name-from-a-relationship-s-target-uri">Resolving a Part Name from a Target URI</a>