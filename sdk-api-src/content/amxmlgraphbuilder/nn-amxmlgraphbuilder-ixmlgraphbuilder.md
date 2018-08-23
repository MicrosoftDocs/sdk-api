---
UID: NN:amxmlgraphbuilder.IXMLGraphBuilder
title: IXMLGraphBuilder
author: windows-sdk-content
description: The IXMLGraphBuilder interface is used to persist a DirectShow filter graph using an XML file format.Note  Support for this interface was removed in Windows 7. New applications should not use this interface. .
old-location: dshow\ixmlgraphbuilder.htm
old-project: DirectShow
ms.assetid: c30a8b33-7783-4987-aa65-ccba476ea937
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IXMLGraphBuilder, IXMLGraphBuilder interface [DirectShow], IXMLGraphBuilder interface [DirectShow],described, IXMLGraphBuilderInterface, amxmlgraphbuilder/IXMLGraphBuilder, dshow.ixmlgraphbuilder
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: amxmlgraphbuilder.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AM_FRAMESTEP_STEP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amxmlgraphbuilder.h
api_name:
 - IXMLGraphBuilder
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IXMLGraphBuilder interface


## -description



The <b>IXMLGraphBuilder</b>  interface is used to persist a DirectShow filter graph using an XML file format.

<div class="alert"><b>Note</b>  Support for this interface was removed in Windows 7. New applications should not use this interface.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXMLGraphBuilder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXMLGraphBuilder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXMLGraphBuilder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/953449da-620e-44cd-880c-b4c13d8bdbf6">BuildFromXML</a>
</td>
<td align="left" width="63%">
Loads a filter graph from an XML element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/238a3077-0f04-44bb-a6ac-b532ef97c315">BuildFromXMLFile</a>
</td>
<td align="left" width="63%">
Loads a filter graph from an XML file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02f710a4-3d13-46b0-b00d-4ffd2b4c3157">SaveToXML</a>
</td>
<td align="left" width="63%">
Saves a filter graph to an XML element.

</td>
</tr>
</table> 


## -remarks



 To get a pointer to this interface, call <b>CoCreateInstance</b> with the class identifier CLSID_XMLGraphBuilder.

The recommended way to save and load a filter graph is to use the GraphEdit file format:

<ul>
<li>
<a href="https://msdn.microsoft.com/f7eeae3c-506b-484c-8fe5-ddd391af5a59">Saving a Filter Graph to a GraphEdit File</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0e1cff4e-43f8-4d0a-b7a7-b6d0278e9e4a">Loading a GraphEdit File Programmatically</a>
</li>
</ul>
Generally, you should persist a filter graph only for testing purposes and not for production. There is no consistently reliable way to reload a filter graph from a file, because the user's hardware and software configurations can change between sessions. Therefore, except for testing, an application should always build a filter graph programmatically.



