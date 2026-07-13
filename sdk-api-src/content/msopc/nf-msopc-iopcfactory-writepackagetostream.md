---
UID: NF:msopc.IOpcFactory.WritePackageToStream
title: IOpcFactory::WritePackageToStream (msopc.h)
description: Serializes a package that is represented by a package object.
helpviewer_keywords: ["IOpcFactory interface [Open Packaging Conventions]","WritePackageToStream method","IOpcFactory.WritePackageToStream","IOpcFactory::WritePackageToStream","WritePackageToStream","WritePackageToStream method [Open Packaging Conventions]","WritePackageToStream method [Open Packaging Conventions]","IOpcFactory interface","msopc/IOpcFactory::WritePackageToStream","opc.iopcfactory_writepackagetostream"]
old-location: opc\iopcfactory_writepackagetostream.htm
tech.root: OPC
ms.assetid: b155700d-3037-4c6e-b2f2-bba39513d7d3
ms.date: 12/05/2018
ms.keywords: IOpcFactory interface [Open Packaging Conventions],WritePackageToStream method, IOpcFactory.WritePackageToStream, IOpcFactory::WritePackageToStream, WritePackageToStream, WritePackageToStream method [Open Packaging Conventions], WritePackageToStream method [Open Packaging Conventions],IOpcFactory interface, msopc/IOpcFactory::WritePackageToStream, opc.iopcfactory_writepackagetostream
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
 - IOpcFactory::WritePackageToStream
 - msopc/IOpcFactory::WritePackageToStream
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
 - IOpcFactory.WritePackageToStream
---

# IOpcFactory::WritePackageToStream


## -description

Serializes a package  that is represented by a package object.

## -parameters

### -param package [in]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpackage">IOpcPackage</a> interface  of the package object that contains data to be serialized.

### -param flags [in]

The value that describes the encoding method  used in serialization.

### -param stream [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface of the stream where the package object  data will be written.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value passed in the <i>flags</i> parameter is not a valid <a href="/windows/win32/api/msopc/ne-msopc-opc_write_flags">OPC_WRITE_FLAGS</a> enumeration value.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the <i>stream</i> and <i>package</i> parameters is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IStream interface error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Package Consumption error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="/previous-versions/windows/desktop/opc/package-consumption-error-group">Package Consumption Error Group</a>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Part URI error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="/previous-versions/windows/desktop/opc/part-uri-error-group">Part URI Error Group</a>. 

</td>
</tr>
</table>

## -remarks

Do not use a stream to serialize package data when the same stream is being used to deserialize a package, because the attempt may result in undefined behavior.

For information about how to use this method to save a package that is represented as a package object, see the <a href="/previous-versions/windows/desktop/opc/saving-a-package">Saving a Package</a> programming task. 

<h3><a id="Support_on_Previous_Versions_of_Windows"></a><a id="support_on_previous_versions_of_windows"></a><a id="SUPPORT_ON_PREVIOUS_VERSIONS_OF_WINDOWS"></a>Support on Previous Versions of Windows</h3>
This method is not supported on versions of Windows prior to Windows 7. For more information, see <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>, and <a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory">IOpcFactory</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_write_flags">OPC_WRITE_FLAGS</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/saving-a-package">Saving a Package</a>