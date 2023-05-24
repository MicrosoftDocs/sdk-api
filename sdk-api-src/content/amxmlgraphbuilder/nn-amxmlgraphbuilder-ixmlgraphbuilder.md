---
UID: NN:amxmlgraphbuilder.IXMLGraphBuilder
title: IXMLGraphBuilder (amxmlgraphbuilder.h)
description: The IXMLGraphBuilder interface is used to persist a DirectShow filter graph using an XML file format.Note  Support for this interface was removed in Windows 7. New applications should not use this interface. .
helpviewer_keywords: ["IXMLGraphBuilder","IXMLGraphBuilder interface [DirectShow]","IXMLGraphBuilder interface [DirectShow]","described","IXMLGraphBuilderInterface","amxmlgraphbuilder/IXMLGraphBuilder","dshow.ixmlgraphbuilder"]
old-location: dshow\ixmlgraphbuilder.htm
tech.root: dshow
ms.assetid: c30a8b33-7783-4987-aa65-ccba476ea937
ms.date: 12/05/2018
ms.keywords: IXMLGraphBuilder, IXMLGraphBuilder interface [DirectShow], IXMLGraphBuilder interface [DirectShow],described, IXMLGraphBuilderInterface, amxmlgraphbuilder/IXMLGraphBuilder, dshow.ixmlgraphbuilder
req.header: amxmlgraphbuilder.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXMLGraphBuilder
 - amxmlgraphbuilder/IXMLGraphBuilder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amxmlgraphbuilder.h
api_name:
 - IXMLGraphBuilder
---

# IXMLGraphBuilder interface


## -description

The <b>IXMLGraphBuilder</b>  interface is used to persist a DirectShow filter graph using an XML file format.

<div class="alert"><b>Note</b>  Support for this interface was removed in Windows 7. New applications should not use this interface.</div>
<div> </div>

## -inheritance

The <b>IXMLGraphBuilder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXMLGraphBuilder</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

 To get a pointer to this interface, call <b>CoCreateInstance</b> with the class identifier CLSID_XMLGraphBuilder.

The recommended way to save and load a filter graph is to use the GraphEdit file format:

<ul>
<li>
<a href="/windows/desktop/DirectShow/saving-a-filter-graph-to-a-graphedit-file">Saving a Filter Graph to a GraphEdit File</a>
</li>
<li>
<a href="/windows/desktop/DirectShow/loading-a-graphedit-file-programmatically">Loading a GraphEdit File Programmatically</a>
</li>
</ul>
Generally, you should persist a filter graph only for testing purposes and not for production. There is no consistently reliable way to reload a filter graph from a file, because the user's hardware and software configurations can change between sessions. Therefore, except for testing, an application should always build a filter graph programmatically.
