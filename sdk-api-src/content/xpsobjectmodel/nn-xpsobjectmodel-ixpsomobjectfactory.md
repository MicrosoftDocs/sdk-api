---
UID: NN:xpsobjectmodel.IXpsOMObjectFactory
title: IXpsOMObjectFactory
author: windows-sdk-content
description: Creates objects in the XPS document object model.
old-location: xps\ixpsomobjectfactory.htm
old-project: printdocs
ms.assetid: 2444703e-4b89-4ef0-9ed7-aa937bc62e8c
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IXpsOMObjectFactory, IXpsOMObjectFactory interface [XPS Documents and Packaging], IXpsOMObjectFactory interface [XPS Documents and Packaging],described, xps.ixpsomobjectfactory, xpsobjectmodel/IXpsOMObjectFactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMObjectFactory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMObjectFactory interface


## -description


Creates objects in    the XPS document object model.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMObjectFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsOMObjectFactory</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1ee3a80d-f6d8-45ba-8178-e3870404698a">CreateCanvas</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/3cb0e1b3-88a8-4724-a3c5-0df416294e62">IXpsOMCanvas</a> interface that is used to group page elements.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb4d1b49-fda6-46c3-a72a-21affdb7e82e">CreateColorProfileResource</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/8a344300-c3fc-4225-bfa5-d5d33798a094">IXpsOMColorProfileResource</a> interface,  which is used to access a color profile resource stream.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7146f0c-e397-45cb-9eb0-e03b3ac0e905">CreateCoreProperties</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a> interface,  which  contains the metadata that describes an XPS document.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0a26f36-b25d-4ab6-9779-88d01d59e41c">CreateDictionary</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface,  which enables the sharing of property resources.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d181c62b-e1a5-45ee-9ffd-85bb6be24892">CreateDocument</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface, which can contain a set of <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interfaces in an ordered sequence.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51d42b34-3380-4464-8feb-d03935f88077">CreateDocumentSequence</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/472095a4-ecd8-406a-97c2-1a34b4e5184a">IXpsOMDocumentSequence</a> interface, which  can contain the <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interfaces of the XPS document.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce41c5fb-033d-4140-b7aa-4f28676f0ae6">CreateDocumentStructureResource</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a> interface, which provides access to the document structure resource stream.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9893716b-5004-4886-9bed-49a447e97f42">CreateFontResource</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/dd0ce1c0-1c04-46a8-9075-93de9b3e3062">IXpsOMFontResource</a> interface, which provides an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface to the font resource.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6933542-eb88-4936-a1d7-8380afc61557">CreateGeometry</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface,  which specifies the shape of a path or of a clipping region.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9138dbc-5a9e-4653-bab2-71f6d716eba6">CreateGeometryFigure</a>
</td>
<td align="left" width="63%">

              Creates an  <a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a> interface, which specifies a portion of an object that is defined by  an  <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b97005dc-a79b-4234-b1a9-8fe705aea518">CreateGlyphs</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a> interface,  which specifies text that appears on a page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9217444-fc9d-4b1e-abb2-7e1badd32052">CreateGradientStop</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a> interface to represent a single color and location definition within a gradient.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f271e152-8120-49c4-804d-069e224c6597">CreateImageBrush</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/f5478582-466b-496e-b7f3-42fb8caa6814">IXpsOMImageBrush</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/267f6e3e-ed1d-4ce7-a554-a943ac3f469d">CreateImageResource</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface, which is used to access an image resource stream.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b829e8fe-5ef0-43d8-b115-9cddbfe1a255">CreateLinearGradientBrush</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/739bf088-0f09-47c1-9b49-6c279395f15b">IXpsOMLinearGradientBrush</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10377a1f-67b4-4fae-81f7-e6bf50e1c2b2">CreateMatrixTransform</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface that specifies an affine matrix transform.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9319997-6c8f-4e2c-9401-ad269e3db8c8">CreatePackage</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a> interface that serves as the root node of an XPS object model document tree.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2498792b-a33c-47cd-8d88-8e89b99c432d">CreatePackageFromFile</a>
</td>
<td align="left" width="63%">
Opens an XPS package file and returns an instantiated XPS document object  tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a4bb128-9480-4e50-8848-a2e1e715f4e3">CreatePackageFromStream</a>
</td>
<td align="left" width="63%">
Opens a stream that contains an XPS package, and returns an instantiated XPS document object  tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67d081a6-ec10-4cd3-8f77-b7653aef27a1">CreatePackageWriterOnFile</a>
</td>
<td align="left" width="63%">
Opens a file for writing the contents of an XPS OM to an XPS package. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77f432e3-7b6a-426f-8673-06dbf3038443">CreatePackageWriterOnStream</a>
</td>
<td align="left" width="63%">
Opens a stream for writing the contents of an XPS OM to an XPS package. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9212ccd8-0793-40cc-bab5-609ea74715f7">CreatePage</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a> interface,  which provides the root node of a tree of objects  that represent the contents of a single page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/daeafc73-33b0-4c88-b92d-da4ca42b19a9">CreatePageFromStream</a>
</td>
<td align="left" width="63%">

              Reads the page markup from the specified stream to create and populate an <a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/037a7926-def4-4be3-b7c5-3c4c588e75ae">CreatePageReference</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interface that enables the virtualization of pages.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f525139b-a94f-41ee-966f-408079a9e676">CreatePartResources</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/9f706f23-25a0-40ee-93f4-3d7ac98ad6ed">IXpsOMPartResources</a> interface that can contain part-based resources.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ed86fd1-ebc0-4eb6-a332-0dea3a21c100">CreatePartUri</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that uses the specified URI.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1127a314-43c8-43a2-a06e-88858a43c519">CreatePartUriCollection</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/05fe9700-19e6-4e63-9693-cfa4b019f643">IXpsOMPartUriCollection</a> interface that can contain <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointers.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa5dcddd-9ca7-4b8f-9f4f-aa0f851e8697">CreatePath</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a> interface that specifies a graphical path element on a page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67d5ccfc-0f01-49d2-966e-09c7958921a5">CreatePrintTicketResource</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface that enables access to a PrintTicket stream.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b91c9490-1995-48cb-a313-ef83f00b9c50">CreateRadialGradientBrush</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/2f5b7b99-64a0-4156-8963-cfceb0d73503">IXpsOMRadialGradientBrush</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00df5162-6fcd-4df8-b7d4-614c14aca8b5">CreateReadOnlyStreamOnFile</a>
</td>
<td align="left" width="63%">

              Creates a read-only <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> over the specified file.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f3f10f0-803a-49e2-bb62-ac4124cb375a">CreateRemoteDictionaryResource</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface that enables the sharing of property resources.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/996a97f5-320f-4e51-af15-f3b125d4f6c8">CreateRemoteDictionaryResourceFromStream</a>
</td>
<td align="left" width="63%">

              Loads the  remote resource dictionary markup into an unrooted <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0948d495-f2da-4361-8365-d4316da72524">CreateSignatureBlockResource</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/f5052470-487d-4f47-8d42-70538a4a45a8">IXpsOMSignatureBlockResource</a> that can contain one or more signature requests.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58690d93-9e3f-487c-956e-bb21122ecc96">CreateSolidColorBrush</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/26580a25-09d1-4a9b-85c3-aa8ddcc97867">IXpsOMSolidColorBrush</a> interface, which specifies a brush of a single, solid color.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0e3f538-4af9-4d86-8899-6ea4e601eaad">CreateStoryFragmentsResource</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/83bc8017-c679-40a8-96a8-bff9aa2273af">IXpsOMStoryFragmentsResource</a> interface that provides access to the story fragments resource stream.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad19841a-629f-4127-a6ea-890168e0c53c">CreateVisualBrush</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/56c11e64-64a8-4c42-9547-4f1fcdc13a4b">IXpsOMVisualBrush</a> interface, which is  an <a href="https://msdn.microsoft.com/fc9e1925-0dbc-447b-9acc-e7f719df62d1">IXpsOMTileBrush</a>  that uses a visual object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/130114DF-DEE7-4ADD-8080-7D804F9F296E">IXpsDocumentPackageTarget::GetXpsOMFactory</a>



<a href="https://msdn.microsoft.com/920d940f-5ae2-4376-8c7b-0cef04f21df7">Initialize an XPS OM</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

