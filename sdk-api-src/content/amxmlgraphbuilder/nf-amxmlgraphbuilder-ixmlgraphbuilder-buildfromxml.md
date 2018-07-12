---
UID: NF:amxmlgraphbuilder.IXMLGraphBuilder.BuildFromXML
title: IXMLGraphBuilder::BuildFromXML
author: windows-sdk-content
description: The BuildFromXML method loads a filter graph from an XML element.
old-location: dshow\ixmlgraphbuilder_buildfromxml.htm
old-project: DirectShow
ms.assetid: 953449da-620e-44cd-880c-b4c13d8bdbf6
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: BuildFromXML, BuildFromXML method [DirectShow], BuildFromXML method [DirectShow],IXMLGraphBuilder interface, IXMLGraphBuilder interface [DirectShow],BuildFromXML method, IXMLGraphBuilder.BuildFromXML, IXMLGraphBuilder::BuildFromXML, IXMLGraphBuilderBuildFromXML, amxmlgraphbuilder/IXMLGraphBuilder::BuildFromXML, dshow.ixmlgraphbuilder_buildfromxml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IXMLGraphBuilder.BuildFromXML
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IXMLGraphBuilder::BuildFromXML


## -description



The <b>BuildFromXML</b> method loads a filter graph from an XML element.


<div class="alert"><b>Note</b>  Support for this interface was removed in Windows 7. New applications should not use this interface.</div><div> </div>

## -parameters




### -param pGraph [in]

Pointer to the Filter Graph Manager's <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface. To create the <a href="https://msdn.microsoft.com/b1a53193-27c6-4e86-a5b9-f3c1e4401690">Filter Graph Manager</a>, call <b>CoCreateInstance</b>. Do not add any filters to the graph before calling this method.


### -param pxml [in]

Pointer to the <b>IXMLElement</b> interface of an XML element object. The XML element object must contain the string returned by the <a href="https://msdn.microsoft.com/02f710a4-3d13-46b0-b00d-4ffd2b4c3157">IXMLGraphBuilder::SaveToXML</a> method.

<div class="alert"><b>Note</b>  The <b>IXMLElement</b> interface is implemented in Microsoft XML Core Services (MSXML) version 1.0 but is not implemented in more recent versions of MSXML.</div>
<div> </div>

## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c30a8b33-7783-4987-aa65-ccba476ea937">IXMLGraphBuilder Interface</a>
 

 

