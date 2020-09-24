---
UID: NF:amxmlgraphbuilder.IXMLGraphBuilder.SaveToXML
title: IXMLGraphBuilder::SaveToXML (amxmlgraphbuilder.h)
description: The SaveToXML method saves a filter graph to an XML element.
helpviewer_keywords: ["IXMLGraphBuilder interface [DirectShow]","SaveToXML method","IXMLGraphBuilder.SaveToXML","IXMLGraphBuilder::SaveToXML","IXMLGraphBuilderSaveToXML","SaveToXML","SaveToXML method [DirectShow]","SaveToXML method [DirectShow]","IXMLGraphBuilder interface","amxmlgraphbuilder/IXMLGraphBuilder::SaveToXML","dshow.ixmlgraphbuilder_savetoxml"]
old-location: dshow\ixmlgraphbuilder_savetoxml.htm
tech.root: dshow
ms.assetid: 02f710a4-3d13-46b0-b00d-4ffd2b4c3157
ms.date: 12/05/2018
ms.keywords: IXMLGraphBuilder interface [DirectShow],SaveToXML method, IXMLGraphBuilder.SaveToXML, IXMLGraphBuilder::SaveToXML, IXMLGraphBuilderSaveToXML, SaveToXML, SaveToXML method [DirectShow], SaveToXML method [DirectShow],IXMLGraphBuilder interface, amxmlgraphbuilder/IXMLGraphBuilder::SaveToXML, dshow.ixmlgraphbuilder_savetoxml
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
 - IXMLGraphBuilder::SaveToXML
 - amxmlgraphbuilder/IXMLGraphBuilder::SaveToXML
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
 - IXMLGraphBuilder.SaveToXML
---

# IXMLGraphBuilder::SaveToXML


## -description

The <b>SaveToXML</b> method saves a filter graph to an XML element.


<div class="alert"><b>Note</b>  Support for this interface was removed in Windows 7. New applications should not use this interface.</div><div> </div>

## -parameters

### -param pGraph [in]

Pointer to the Filter Graph Manager's <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface.

### -param pbstrxml [out]

Pointer to a <b>BSTR</b> that receives the XML element. The caller must release the string by calling <b>SysFreeString</b>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amxmlgraphbuilder/nn-amxmlgraphbuilder-ixmlgraphbuilder">IXMLGraphBuilder Interface</a>