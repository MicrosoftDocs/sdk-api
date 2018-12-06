---
UID: NF:wmpservices.IWMPGraphCreation.GraphCreationPostRender
title: IWMPGraphCreation::GraphCreationPostRender
author: windows-sdk-content
description: The GraphCreationPostRender method is called by Windows Media Player after a file has been rendered.
old-location: wmp\iwmpgraphcreation_graphcreationpostrender.htm
tech.root: WMP
ms.assetid: 243fc72e-ef97-49a6-9a50-05ec338e5faa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GraphCreationPostRender, GraphCreationPostRender method [Windows Media Player], GraphCreationPostRender method [Windows Media Player],IWMPGraphCreation interface, IWMPGraphCreation interface [Windows Media Player],GraphCreationPostRender method, IWMPGraphCreation.GraphCreationPostRender, IWMPGraphCreation::GraphCreationPostRender, IWMPGraphCreationGraphCreationPostRenderdeprecated, wmp.iwmpgraphcreation_graphcreationpostrender, wmpservices/IWMPGraphCreation::GraphCreationPostRender
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmpservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later
req.target-min-winversvr: 
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
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPGraphCreation.GraphCreationPostRender
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPGraphCreation::GraphCreationPostRender


## -description


The <b>GraphCreationPostRender</b> method is called by Windows Media Player after a file has been rendered.


## -parameters




### -param pFilterGraph [in]

Pointer to the <b>IUnknown</b> interface of the Windows Media Player control's DirectShow filter graph.


## -returns



Return a success <b>HRESULT</b> code to allow playback to continue or a failure code to terminate playback.




## -remarks



You can call <b>QueryInterface</b> through <i>pFilterGraph</i> to retrieve the DirectShow filter graph interfaces you need.

There is no guarantee that this method will be invoked for all files.  Only files rendered with DirectShow will cause this method to be invoked and the WMPGC_FLAGS_USE_CUSTOM_GRAPH flag to be honored. CD, DVD, Image, Flash, Windows Media Format SDK, and Media Foundation playback will not invoke this method.


<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/80d6f1f0-10c9-4e60-9bb7-556e340730a8">IWMPGraphCreation Interface</a>
 

 

