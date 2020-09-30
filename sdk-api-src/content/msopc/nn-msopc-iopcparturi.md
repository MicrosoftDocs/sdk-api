---
UID: NN:msopc.IOpcPartUri
title: IOpcPartUri (msopc.h)
description: Represents the part name of a part.
helpviewer_keywords: ["IOpcPartUri","IOpcPartUri interface [Open Packaging Conventions]","IOpcPartUri interface [Open Packaging Conventions]","described","msopc/IOpcPartUri","opc.iopcparturi"]
old-location: opc\iopcparturi.htm
tech.root: OPC
ms.assetid: 81123212-7a32-4833-b81f-8454a544327d
ms.date: 12/05/2018
ms.keywords: IOpcPartUri, IOpcPartUri interface [Open Packaging Conventions], IOpcPartUri interface [Open Packaging Conventions],described, msopc/IOpcPartUri, opc.iopcparturi
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
 - IOpcPartUri
 - msopc/IOpcPartUri
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
 - IOpcPartUri
---

# IOpcPartUri interface


## -description

Represents the part name of a part.  If the part is a Relationships part, it is represented by the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipset">IOpcRelationshipSet</a> interface; otherwise, it is represented by the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcPartUri</b> interface inherits from <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcuri">IOpcUri</a>. <b>IOpcPartUri</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcPartUri</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcparturi-compareparturi">ComparePartUri</a>
</td>
<td align="left" width="63%">
Returns an integer that indicates whether the URIs represented by the current part URI object and a specified part URI object are equivalent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcparturi-getsourceuri">GetSourceUri</a>
</td>
<td align="left" width="63%">
              Gets  the source URI of the relationships that are stored in a  Relationships part. The  current part URI object represents the part name of that Relationships part.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcparturi-isrelationshipsparturi">IsRelationshipsPartUri</a>
</td>
<td align="left" width="63%">
Returns a value that indicates whether the current part URI object represents the part name of a Relationships part.

</td>
</tr>
</table>

## -remarks

<h3><a id="Support_on__Previous_Windows_Versions"></a><a id="support_on__previous_windows_versions"></a><a id="SUPPORT_ON__PREVIOUS_WINDOWS_VERSIONS"></a>Support on  Previous Windows Versions</h3>
The behavior and performance of this interface is the same on all supported Windows versions. For more information, see <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>, and <a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcfactory-createparturi">IOpcFactory::CreatePartUri</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcpart-getname">IOpcPart::GetName</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcuri">IOpcUri</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a>



<a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>



<b>Reference</b>