---
UID: NF:msopc.IOpcFactory.CreatePackage
title: IOpcFactory::CreatePackage (msopc.h)
description: Creates a package object that represents an empty package.
helpviewer_keywords: ["CreatePackage","CreatePackage method [Open Packaging Conventions]","CreatePackage method [Open Packaging Conventions]","IOpcFactory interface","IOpcFactory interface [Open Packaging Conventions]","CreatePackage method","IOpcFactory.CreatePackage","IOpcFactory::CreatePackage","msopc/IOpcFactory::CreatePackage","opc.iopcfactory_createpackage"]
old-location: opc\iopcfactory_createpackage.htm
tech.root: OPC
ms.assetid: 9cd4ef3a-f890-40d5-a398-cb8f9746c380
ms.date: 12/05/2018
ms.keywords: CreatePackage, CreatePackage method [Open Packaging Conventions], CreatePackage method [Open Packaging Conventions],IOpcFactory interface, IOpcFactory interface [Open Packaging Conventions],CreatePackage method, IOpcFactory.CreatePackage, IOpcFactory::CreatePackage, msopc/IOpcFactory::CreatePackage, opc.iopcfactory_createpackage
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IOpcFactory::CreatePackage
 - msopc/IOpcFactory::CreatePackage
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
 - IOpcFactory.CreatePackage
---

# IOpcFactory::CreatePackage


## -description

Creates a package object that represents an empty package.

## -parameters

### -param package [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpackage">IOpcPackage</a> interface of the package object that represents an empty package.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not implemented for this version of Windows.

</td>
</tr>
</table>

## -remarks

<h3><a id="Support_on_Previous_Versions_of_Windows"></a><a id="support_on_previous_versions_of_windows"></a><a id="SUPPORT_ON_PREVIOUS_VERSIONS_OF_WINDOWS"></a>Support on Previous Versions of Windows</h3>
This method is not supported on versions of Windows prior to Windows 7. For more information, see <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>, and <a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory">IOpcFactory</a>



<a href="/previous-versions/windows/desktop/opc/music-bundle-sample">Music Bundle Sample</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packages-overview">Packages Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>



<b>Reference</b>