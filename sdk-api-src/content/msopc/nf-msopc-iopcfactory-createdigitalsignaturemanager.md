---
UID: NF:msopc.IOpcFactory.CreateDigitalSignatureManager
title: IOpcFactory::CreateDigitalSignatureManager (msopc.h)
description: Creates a digital signature manager object for a package object.
helpviewer_keywords: ["CreateDigitalSignatureManager","CreateDigitalSignatureManager method [Open Packaging Conventions]","CreateDigitalSignatureManager method [Open Packaging Conventions]","IOpcFactory interface","IOpcFactory interface [Open Packaging Conventions]","CreateDigitalSignatureManager method","IOpcFactory.CreateDigitalSignatureManager","IOpcFactory::CreateDigitalSignatureManager","msopc/IOpcFactory::CreateDigitalSignatureManager","opc.iopcfactory_createdigitalsignaturemanager"]
old-location: opc\iopcfactory_createdigitalsignaturemanager.htm
tech.root: OPC
ms.assetid: ec0fe8b6-e968-4bcb-b468-bbf72ffce675
ms.date: 12/05/2018
ms.keywords: CreateDigitalSignatureManager, CreateDigitalSignatureManager method [Open Packaging Conventions], CreateDigitalSignatureManager method [Open Packaging Conventions],IOpcFactory interface, IOpcFactory interface [Open Packaging Conventions],CreateDigitalSignatureManager method, IOpcFactory.CreateDigitalSignatureManager, IOpcFactory::CreateDigitalSignatureManager, msopc/IOpcFactory::CreateDigitalSignatureManager, opc.iopcfactory_createdigitalsignaturemanager
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
 - IOpcFactory::CreateDigitalSignatureManager
 - msopc/IOpcFactory::CreateDigitalSignatureManager
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
 - IOpcFactory.CreateDigitalSignatureManager
---

# IOpcFactory::CreateDigitalSignatureManager


## -description

Creates a digital signature manager object for a package object.

## -parameters

### -param package [in]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpackage">IOpcPackage</a> interface of the package object to associate with the digital signature manager object.

### -param signatureManager [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignaturemanager">IOpcDigitalSignatureManager</a> interface of the digital signature manager object that is created for use with the package object.

A digital signature manager object provides access to the Packaging API's digital signature interfaces and methods. These can be used to sign the package represented by the package object or to validate the signatures in a package that has already been signed.

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
<dt><b>OPC_E_DS_DUPLICATE_SIGNATURE_ORIGIN_RELATIONSHIP</b></dt>
<dt>0x8051001B</dt>
</dl>
</td>
<td width="60%">
More than one relationship of the digital signature origin relationship type  exists, but only one such relationship is allowed.

For more information about this relationship type, see the <i>OPC</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_INVALID_SIGNATURE_ORIGIN_RELATIONSHIP</b></dt>
<dt>0x8051001C</dt>
</dl>
</td>
<td width="60%">
A package relationship of type digital signature origin is targeting a location that is external to the package. Digital Signature Origin parts must be located internally.

For more information about this relationship type, see the <i>OPC</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_MISSING_SIGNATURE_ORIGIN_PART</b></dt>
<dt>0x8051001F</dt>
</dl>
</td>
<td width="60%">
A relationship of type digital signature origin  was found, but the Digital Signature Origin part itself was not.

For more information about this relationship type, see the <i>OPC</i>.

</td>
</tr>
</table>

## -remarks

If a package is modified while <a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a> are being used to sign the package, signing may fail or result in an inconsistent signature or package.

<h3><a id="Support_on_Previous_Versions_of_Windows"></a><a id="support_on_previous_versions_of_windows"></a><a id="SUPPORT_ON_PREVIOUS_VERSIONS_OF_WINDOWS"></a>Support on Previous Versions of Windows</h3>
This method is not supported on versions of Windows prior to Windows 7. For more information, see <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>, and <a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory">IOpcFactory</a>



<a href="/previous-versions/windows/desktop/opc/music-bundle-signature-sample">Music Bundle Signature Sample</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>



<b>Reference</b>