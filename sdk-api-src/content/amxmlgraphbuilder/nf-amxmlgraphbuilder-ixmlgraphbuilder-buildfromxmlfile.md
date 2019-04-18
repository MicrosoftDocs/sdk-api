---
UID: NF:amxmlgraphbuilder.IXMLGraphBuilder.BuildFromXMLFile
title: IXMLGraphBuilder::BuildFromXMLFile (amxmlgraphbuilder.h)
author: windows-sdk-content
description: The BuildFromXMLFile method loads a filter graph from an XML file.
old-location: dshow\ixmlgraphbuilder_buildfromxmlfile.htm
tech.root: DirectShow
ms.assetid: 238a3077-0f04-44bb-a6ac-b532ef97c315
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BuildFromXMLFile, BuildFromXMLFile method [DirectShow], BuildFromXMLFile method [DirectShow],IXMLGraphBuilder interface, IXMLGraphBuilder interface [DirectShow],BuildFromXMLFile method, IXMLGraphBuilder.BuildFromXMLFile, IXMLGraphBuilder::BuildFromXMLFile, IXMLGraphBuilderBuildFromXMLFile, amxmlgraphbuilder/IXMLGraphBuilder::BuildFromXMLFile, dshow.ixmlgraphbuilder_buildfromxmlfile
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amxmlgraphbuilder.h
api_name:
 - IXMLGraphBuilder.BuildFromXMLFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXMLGraphBuilder::BuildFromXMLFile


## -description



The <b>BuildFromXMLFile</b> method loads a filter graph from an XML file.


<div class="alert"><b>Note</b>  Support for this interface was removed in Windows 7. New applications should not use this interface.</div><div> </div>

## -parameters




### -param pGraph [in]

Pointer to the Filter Graph Manager's <a href="https://msdn.microsoft.com/en-us/library/Dd390085(v=VS.85).aspx">IGraphBuilder</a> interface. To create the <a href="https://msdn.microsoft.com/b1a53193-27c6-4e86-a5b9-f3c1e4401690">Filter Graph Manager</a>, call <b>CoCreateInstance</b>. Do not add any filters to the graph before calling this method.


### -param wszFileName [in]

Wide-character string that contains the full path name of an XML file. The XML file must contain the string returned by the <a href="https://msdn.microsoft.com/en-us/library/Dd390625(v=VS.85).aspx">IXMLGraphBuilder::SaveToXML</a> method.


### -param wszBaseURL [in]

Reserved. Set to <b>NULL</b>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390622(v=VS.85).aspx">IXMLGraphBuilder Interface</a>
 

 

