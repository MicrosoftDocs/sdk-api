---
UID: NN:xpsobjectmodel.IXpsOMObjectFactory
title: IXpsOMObjectFactory (xpsobjectmodel.h)
author: windows-sdk-content
description: Creates objects in the XPS document object model.
old-location: xps\ixpsomobjectfactory.htm
tech.root: printdocs
ms.assetid: 2444703e-4b89-4ef0-9ed7-aa937bc62e8c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMObjectFactory, IXpsOMObjectFactory interface [XPS Documents and Packaging], IXpsOMObjectFactory interface [XPS Documents and Packaging],described, xps.ixpsomobjectfactory, xpsobjectmodel/IXpsOMObjectFactory
ms.topic: interface
f1_keywords: 
 - "xpsobjectmodel/IXpsOMObjectFactory"
dev_langs:
 - c++
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMObjectFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMObjectFactory interface


## -description


Creates objects in    the XPS document object model.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMObjectFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsOMObjectFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMObjectFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createcanvas">CreateCanvas</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas">IXpsOMCanvas</a> interface that is used to group page elements.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createcolorprofileresource">CreateColorProfileResource</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a> interface,  which is used to access a color profile resource stream.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createcoreproperties">CreateCoreProperties</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a> interface,  which  contains the metadata that describes an XPS document.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createdictionary">CreateDictionary</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface,  which enables the sharing of property resources.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createdocument">CreateDocument</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a> interface, which can contain a set of <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a> interfaces in an ordered sequence.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createdocumentsequence">CreateDocumentSequence</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a> interface, which  can contain the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a> interfaces of the XPS document.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createdocumentstructureresource">CreateDocumentStructureResource</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a> interface, which provides access to the document structure resource stream.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createfontresource">CreateFontResource</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a> interface, which provides an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface to the font resource.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-creategeometry">CreateGeometry</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a> interface,  which specifies the shape of a path or of a clipping region.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-creategeometryfigure">CreateGeometryFigure</a>
</td>
<td align="left" width="63%">
Creates an  <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a> interface, which specifies a portion of an object that is defined by  an  <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createglyphs">CreateGlyphs</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a> interface,  which specifies text that appears on a page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-creategradientstop">CreateGradientStop</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a> interface to represent a single color and location definition within a gradient.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createimagebrush">CreateImageBrush</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush">IXpsOMImageBrush</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createimageresource">CreateImageResource</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface, which is used to access an image resource stream.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createlineargradientbrush">CreateLinearGradientBrush</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush">IXpsOMLinearGradientBrush</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-creatematrixtransform">CreateMatrixTransform</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a> interface that specifies an affine matrix transform.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackage">CreatePackage</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a> interface that serves as the root node of an XPS object model document tree.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile">CreatePackageFromFile</a>
</td>
<td align="left" width="63%">
Opens an XPS package file and returns an instantiated XPS document object  tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream">CreatePackageFromStream</a>
</td>
<td align="left" width="63%">
Opens a stream that contains an XPS package, and returns an instantiated XPS document object  tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronfile">CreatePackageWriterOnFile</a>
</td>
<td align="left" width="63%">
Opens a file for writing the contents of an XPS OM to an XPS package. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream">CreatePackageWriterOnStream</a>
</td>
<td align="left" width="63%">
Opens a stream for writing the contents of an XPS OM to an XPS package. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpage">CreatePage</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface,  which provides the root node of a tree of objects  that represent the contents of a single page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpagefromstream">CreatePageFromStream</a>
</td>
<td align="left" width="63%">
Reads the page markup from the specified stream to create and populate an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpagereference">CreatePageReference</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a> interface that enables the virtualization of pages.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpartresources">CreatePartResources</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources">IXpsOMPartResources</a> interface that can contain part-based resources.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createparturi">CreatePartUri</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that uses the specified URI.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createparturicollection">CreatePartUriCollection</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection">IXpsOMPartUriCollection</a> interface that can contain <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointers.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpath">CreatePath</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a> interface that specifies a graphical path element on a page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createprintticketresource">CreatePrintTicketResource</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface that enables access to a PrintTicket stream.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush">CreateRadialGradientBrush</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createreadonlystreamonfile">CreateReadOnlyStreamOnFile</a>
</td>
<td align="left" width="63%">
Creates a read-only <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> over the specified file.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createremotedictionaryresource">CreateRemoteDictionaryResource</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface that enables the sharing of property resources.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createremotedictionaryresourcefromstream">CreateRemoteDictionaryResourceFromStream</a>
</td>
<td align="left" width="63%">
Loads the  remote resource dictionary markup into an unrooted <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createsignatureblockresource">CreateSignatureBlockResource</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresource">IXpsOMSignatureBlockResource</a> that can contain one or more signature requests.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createsolidcolorbrush">CreateSolidColorBrush</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush">IXpsOMSolidColorBrush</a> interface, which specifies a brush of a single, solid color.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createstoryfragmentsresource">CreateStoryFragmentsResource</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a> interface that provides access to the story fragments resource stream.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createvisualbrush">CreateVisualBrush</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush">IXpsOMVisualBrush</a> interface, which is  an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush">IXpsOMTileBrush</a>  that uses a visual object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsdocumentpackagetarget-getxpsomfactory">IXpsDocumentPackageTarget::GetXpsOMFactory</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372970(v=vs.85)">Initialize an XPS OM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

