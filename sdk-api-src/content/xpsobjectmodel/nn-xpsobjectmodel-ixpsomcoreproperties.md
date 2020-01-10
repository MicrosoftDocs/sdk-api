---
UID: NN:xpsobjectmodel.IXpsOMCoreProperties
title: IXpsOMCoreProperties (xpsobjectmodel.h)
description: This interface provides access to the metadata that is stored in the Core Properties part of the XPS document.
old-location: xps\ixpsomcoreproperties.htm
tech.root: printdocs
ms.assetid: 705ec9c7-5aa9-4fc5-ad2c-441cb545d056
ms.date: 12/05/2018
ms.keywords: IXpsOMCoreProperties, IXpsOMCoreProperties interface [XPS Documents and Packaging], IXpsOMCoreProperties interface [XPS Documents and Packaging],described, xps.ixpsomcoreproperties, xpsobjectmodel/IXpsOMCoreProperties
f1_keywords:
- xpsobjectmodel/IXpsOMCoreProperties
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
- IXpsOMCoreProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMCoreProperties interface


## -description


This interface provides access to the metadata that is stored in the Core Properties part of the XPS document.

The contents of the Core Properties part are described in  the 1st edition, Part 2, "Open Packaging Conventions," of <a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMCoreProperties</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart">IXpsOMPart</a>. <b>IXpsOMCoreProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMCoreProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-clone">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-getcategory">GetCategory</a>
</td>
<td align="left" width="63%">
Gets the <b>category</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-getcontentstatus">GetContentStatus</a>
</td>
<td align="left" width="63%">
Gets the <b>contentStatus</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-getcontenttype">GetContentType</a>
</td>
<td align="left" width="63%">
Gets the <b>contentType</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-getcreated">GetCreated</a>
</td>
<td align="left" width="63%">
Gets the <b>created</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-getcreator">GetCreator</a>
</td>
<td align="left" width="63%">
Gets the <b>creator</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Gets the <b>description</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-getidentifier">GetIdentifier</a>
</td>
<td align="left" width="63%">
Gets the <b>identifier</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-getkeywords">GetKeywords</a>
</td>
<td align="left" width="63%">
Gets the <b>keywords</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-getlanguage">GetLanguage</a>
</td>
<td align="left" width="63%">
Gets the <b>language</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-getlastmodifiedby">GetLastModifiedBy</a>
</td>
<td align="left" width="63%">
Gets the <b>lastModifiedBy</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-getlastprinted">GetLastPrinted</a>
</td>
<td align="left" width="63%">
Gets the <b>lastPrinted</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-getmodified">GetModified</a>
</td>
<td align="left" width="63%">
Gets the <b>modified</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-getowner">GetOwner</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a> interface that contains the core properties.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-getrevision">GetRevision</a>
</td>
<td align="left" width="63%">
Gets the <b>revision</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-getsubject">GetSubject</a>
</td>
<td align="left" width="63%">
Gets the <b>subject</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-gettitle">GetTitle</a>
</td>
<td align="left" width="63%">
Gets the <b>title</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-getversion">GetVersion</a>
</td>
<td align="left" width="63%">
Gets the <b>version</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-setcategory">SetCategory</a>
</td>
<td align="left" width="63%">
Sets the <b>category</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-setcontentstatus">SetContentStatus</a>
</td>
<td align="left" width="63%">
Sets the <b>contentStatus</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-setcontenttype">SetContentType</a>
</td>
<td align="left" width="63%">
Sets the <b>contentType</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-setcreated">SetCreated</a>
</td>
<td align="left" width="63%">
Sets the <b>created</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-setcreator">SetCreator</a>
</td>
<td align="left" width="63%">
Sets the <b>creator</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-setdescription">SetDescription</a>
</td>
<td align="left" width="63%">
Sets the <b>description</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-setidentifier">SetIdentifier</a>
</td>
<td align="left" width="63%">
Sets the <b>identifier</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-setkeywords">SetKeywords</a>
</td>
<td align="left" width="63%">
Sets the <b>keywords</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-setlanguage">SetLanguage</a>
</td>
<td align="left" width="63%">
Sets the <b>language</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-setlastmodifiedby">SetLastModifiedBy</a>
</td>
<td align="left" width="63%">
Sets the <b>lastModifiedBy</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-setlastprinted">SetLastPrinted</a>
</td>
<td align="left" width="63%">
Sets the <b>lastPrinted</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-setmodified">SetModified</a>
</td>
<td align="left" width="63%">
Sets the <b>modified</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-setrevision">SetRevision</a>
</td>
<td align="left" width="63%">
Sets the <b>revision</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-setsubject">SetSubject</a>
</td>
<td align="left" width="63%">
Sets the <b>subject</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-settitle">SetTitle</a>
</td>
<td align="left" width="63%">
Sets the <b>title</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcoreproperties-setversion">SetVersion</a>
</td>
<td align="left" width="63%">
Sets the <b>version</b> property.
            

</td>
</tr>
</table> 


## -remarks



The meaning and use of these properties is determined by the user or context.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createcoreproperties">IXpsOMObjectFactory::CreateCoreProperties</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart">IXpsOMPart</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

