---
UID: NF:msopc.IOpcFactory.CreatePackageRootUri
title: IOpcFactory::CreatePackageRootUri (msopc.h)
description: Creates an OPC URI object that represents the root of a package.
helpviewer_keywords: ["CreatePackageRootUri","CreatePackageRootUri method [Open Packaging Conventions]","CreatePackageRootUri method [Open Packaging Conventions]","IOpcFactory interface","IOpcFactory interface [Open Packaging Conventions]","CreatePackageRootUri method","IOpcFactory.CreatePackageRootUri","IOpcFactory::CreatePackageRootUri","msopc/IOpcFactory::CreatePackageRootUri","opc.iopcfactory_createpackagerooturi"]
old-location: opc\iopcfactory_createpackagerooturi.htm
tech.root: OPC
ms.assetid: 5ec33743-d362-43d9-a66e-8223745b9664
ms.date: 12/05/2018
ms.keywords: CreatePackageRootUri, CreatePackageRootUri method [Open Packaging Conventions], CreatePackageRootUri method [Open Packaging Conventions],IOpcFactory interface, IOpcFactory interface [Open Packaging Conventions],CreatePackageRootUri method, IOpcFactory.CreatePackageRootUri, IOpcFactory::CreatePackageRootUri, msopc/IOpcFactory::CreatePackageRootUri, opc.iopcfactory_createpackagerooturi
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
 - IOpcFactory::CreatePackageRootUri
 - msopc/IOpcFactory::CreatePackageRootUri
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
 - IOpcFactory.CreatePackageRootUri
---

# IOpcFactory::CreatePackageRootUri


## -description

Creates an OPC URI object that represents the root of  a package.

## -parameters

### -param rootUri [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcuri">IOpcUri</a> interface of the OPC URI object that represents the URI of the root of a package.

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
The <i>rootUri</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The URI of the root of a package is always represented as "/".

<h3><a id="Support_on__Previous_Windows_Versions"></a><a id="support_on__previous_windows_versions"></a><a id="SUPPORT_ON__PREVIOUS_WINDOWS_VERSIONS"></a>Support on  Previous Windows Versions</h3>
The behavior and performance of this method is the same on all supported Windows versions. For more information, see <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>, and <a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory">IOpcFactory</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>



<b>Reference</b>