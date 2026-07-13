---
UID: NN:msopc.IOpcFactory
title: IOpcFactory (msopc.h)
description: Creates Packaging API objects and provides support for saving and loading packages.
helpviewer_keywords: ["IOpcFactory","IOpcFactory interface [Open Packaging Conventions]","IOpcFactory interface [Open Packaging Conventions]","described","msopc/IOpcFactory","opc.iopcfactory"]
old-location: opc\iopcfactory.htm
tech.root: OPC
ms.assetid: 0a265a0a-c109-4afc-a0ad-d3ee31757aa1
ms.date: 12/05/2018
ms.keywords: IOpcFactory, IOpcFactory interface [Open Packaging Conventions], IOpcFactory interface [Open Packaging Conventions],described, msopc/IOpcFactory, opc.iopcfactory
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
 - IOpcFactory
 - msopc/IOpcFactory
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
 - IOpcFactory
---

# IOpcFactory interface


## -description

Creates Packaging API objects and provides support for saving and loading packages.  Objects that are created by <b>IOpcFactory</b> interface methods provide support for creating, populating, modifying, and digitally signing packages.

## -inheritance

The <b>IOpcFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcFactory</b> also has these types of members:

## -remarks

Do not use a stream to serialize package data when the same stream is being used to deserialize a package; attempting to do so may result in undefined behavior.

To use the Packaging API, the package must map to a ZIP archive as specified in the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.

To create a factory that implements the <b>IOpcFactory</b> interface,  call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function. This factory is not tied to any particular package or Packaging API object, and it can be used for the lifetime of the application. For example code that shows how to create a factory implementing  <b>IOpcFactory</b>, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

<h3><a id="IOpcFactory_Support_on_Previous_Versions_of_Windows"></a><a id="iopcfactory_support_on_previous_versions_of_windows"></a><a id="IOPCFACTORY_SUPPORT_ON_PREVIOUS_VERSIONS_OF_WINDOWS"></a>IOpcFactory Support on Previous Versions of Windows</h3>
If an application attempts to an unsupported <b>IOpcFactory</b> method, the E_NOTIMPL error code will be returned. For more information, see <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>, and <a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignaturemanager">IOpcDigitalSignatureManager</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpackage">IOpcPackage</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcuri">IOpcUri</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>



<b>Reference</b>
