---
UID: NN:xpsobjectmodel_1.IXpsOMObjectFactory1
title: IXpsOMObjectFactory1 (xpsobjectmodel_1.h)
description: Inherits from IXpsOMObjectFactory.
helpviewer_keywords: ["IXpsOMObjectFactory1","IXpsOMObjectFactory1 interface [XPS Documents and Packaging]","IXpsOMObjectFactory1 interface [XPS Documents and Packaging]","described","xps.ixpsomobjectfactory1","xpsobjectmodel_1/IXpsOMObjectFactory1"]
old-location: xps\ixpsomobjectfactory1.htm
tech.root: xps
ms.assetid: f013e59d-83ae-453f-9cc5-9a8230729128
ms.date: 12/05/2018
ms.keywords: IXpsOMObjectFactory1, IXpsOMObjectFactory1 interface [XPS Documents and Packaging], IXpsOMObjectFactory1 interface [XPS Documents and Packaging],described, xps.ixpsomobjectfactory1, xpsobjectmodel_1/IXpsOMObjectFactory1
req.header: xpsobjectmodel_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: None
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMObjectFactory1
 - xpsobjectmodel_1/IXpsOMObjectFactory1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - none
 - none.dll
api_name:
 - IXpsOMObjectFactory1
---

# IXpsOMObjectFactory1 interface

## -description

Inherits from IXpsOMObjectFactory. 

Adds support for:

Detecting the type of an XPS package. 

Loading of an OpenXPS packages into an XPS object model. 

Saving an in-memory XPS Object model to an OpenXPS package. 

Converting HDPhoto resources into JpegXR resources.

## -inheritance

The <b>IXpsOMObjectFactory1</b> interface inherits from <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>. <b>IXpsOMObjectFactory1</b> also has these types of members:

## -members

The <b>IXpsOMObjectFactory1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-converthdphototojpegxr">IXpsOMObjectFactory1::ConvertHDPhotoToJpegXR</a>
</td>
<td align="left" width="63%">
Converts an image resource from an HD Photo to a JpegXR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-convertjpegxrtohdphoto">IXpsOMObjectFactory1::ConvertJpegXRToHDPhoto</a>
</td>
<td align="left" width="63%">
Converts an image resource from a JpegXR to an HD Photo.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-createpackagefromfile1">IXpsOMObjectFactory1::CreatePackageFromFile1</a>
</td>
<td align="left" width="63%">
Opens an XPS package file and returns an instantiated XPS document object tree. This method will read a file that contains an XPS document that is of type XPS_DOCUMENT_TYPE_ XPS or XPS_DOCUMENT_TYPE_ OPENXPS

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-createpackagefromstream1">IXpsOMObjectFactory1::CreatePackageFromStream1</a>
</td>
<td align="left" width="63%">
Opens a stream that contains an XPS package and returns an instantiated XPS document object tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-createpackagewriteronfile1">IXpsOMObjectFactory1::CreatePackageWriterOnFile1</a>
</td>
<td align="left" width="63%">
Opens a file for writing the contents of an XPS OM to an XPS package of a specified type. This method produces a package writer for either an MSXPS document or an OpenXPS document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-createpackagewriteronstream1">IXpsOMObjectFactory1::CreatePackageWriterOnStream1</a>
</td>
<td align="left" width="63%">
Opens a stream for writing the contents of an XPS OM to an XPS package of a specified type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-createpagefromstream1">IXpsOMObjectFactory1::CreatePageFromStream1</a>
</td>
<td align="left" width="63%">
Reads the page markup from the specified stream to create and populate an IXpsOMPage1 interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-createremotedictionaryresourcefromstream1">IXpsOMObjectFactory1::CreateRemoteDictionaryResourceFromStream1</a>
</td>
<td align="left" width="63%">
Loads the remote resource dictionary markup into an unrooted IXpsOMRemoteDictionaryResource interface. The dictionary referenced by the dictionaryMarkupStream parameter can contain markup from either the OpenXPS or the MSXPS namespace. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile">IXpsOMObjectFactory1::GetDocumentTypeFromFile</a>
</td>
<td align="left" width="63%">
Detects the type of XPS document that is stored in the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream">IXpsOMObjectFactory1::GetDocumentTypeFromStream</a>
</td>
<td align="left" width="63%">
Detects the type of XPS document that is stored in the specified stream.

</td>
</tr>
</table>

## -members

The <b>IXpsOMObjectFactory1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-converthdphototojpegxr">IXpsOMObjectFactory1::ConvertHDPhotoToJpegXR</a>
</td>
<td align="left" width="63%">
Converts an image resource from an HD Photo to a JpegXR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-convertjpegxrtohdphoto">IXpsOMObjectFactory1::ConvertJpegXRToHDPhoto</a>
</td>
<td align="left" width="63%">
Converts an image resource from a JpegXR to an HD Photo.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-createpackagefromfile1">IXpsOMObjectFactory1::CreatePackageFromFile1</a>
</td>
<td align="left" width="63%">
Opens an XPS package file and returns an instantiated XPS document object tree. This method will read a file that contains an XPS document that is of type XPS_DOCUMENT_TYPE_ XPS or XPS_DOCUMENT_TYPE_ OPENXPS

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-createpackagefromstream1">IXpsOMObjectFactory1::CreatePackageFromStream1</a>
</td>
<td align="left" width="63%">
Opens a stream that contains an XPS package and returns an instantiated XPS document object tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-createpackagewriteronfile1">IXpsOMObjectFactory1::CreatePackageWriterOnFile1</a>
</td>
<td align="left" width="63%">
Opens a file for writing the contents of an XPS OM to an XPS package of a specified type. This method produces a package writer for either an MSXPS document or an OpenXPS document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-createpackagewriteronstream1">IXpsOMObjectFactory1::CreatePackageWriterOnStream1</a>
</td>
<td align="left" width="63%">
Opens a stream for writing the contents of an XPS OM to an XPS package of a specified type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-createpagefromstream1">IXpsOMObjectFactory1::CreatePageFromStream1</a>
</td>
<td align="left" width="63%">
Reads the page markup from the specified stream to create and populate an IXpsOMPage1 interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-createremotedictionaryresourcefromstream1">IXpsOMObjectFactory1::CreateRemoteDictionaryResourceFromStream1</a>
</td>
<td align="left" width="63%">
Loads the remote resource dictionary markup into an unrooted IXpsOMRemoteDictionaryResource interface. The dictionary referenced by the dictionaryMarkupStream parameter can contain markup from either the OpenXPS or the MSXPS namespace. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile">IXpsOMObjectFactory1::GetDocumentTypeFromFile</a>
</td>
<td align="left" width="63%">
Detects the type of XPS document that is stored in the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream">IXpsOMObjectFactory1::GetDocumentTypeFromStream</a>
</td>
<td align="left" width="63%">
Detects the type of XPS document that is stored in the specified stream.

</td>
</tr>
</table>

## -remarks

<h3><a id="Additional_References"></a><a id="additional_references"></a><a id="ADDITIONAL_REFERENCES"></a>Additional References</h3>
The base interface is defined and documented in Windows 7 SDK.

[IXpsOMObjectFactory interface](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>
