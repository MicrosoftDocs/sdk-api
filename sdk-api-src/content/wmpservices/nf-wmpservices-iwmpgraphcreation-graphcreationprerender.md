---
UID: NF:wmpservices.IWMPGraphCreation.GraphCreationPreRender
title: IWMPGraphCreation::GraphCreationPreRender method
author: windows-driver-content
description: The GraphCreationPreRender method is called by Windows Media Player before a file is rendered.
old-location: wmp\iwmpgraphcreation_graphcreationprerender.htm
old-project: WMP
ms.assetid: d3375fa9-2ab0-4e82-9196-0b3971a00185
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: GraphCreationPreRender method [Windows Media Player], GraphCreationPreRender method [Windows Media Player], IWMPGraphCreation interface, GraphCreationPreRender,IWMPGraphCreation.GraphCreationPreRender, IWMPGraphCreation, IWMPGraphCreation interface [Windows Media Player], GraphCreationPreRender method, IWMPGraphCreation::GraphCreationPreRender, IWMPGraphCreationGraphCreationPreRenderdeprecated, wmp.iwmpgraphcreation_graphcreationprerender, wmpservices/IWMPGraphCreation::GraphCreationPreRender
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
req.typenames: WMPServices_StreamState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPGraphCreation.GraphCreationPreRender
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPGraphCreation::GraphCreationPreRender method


## -description



        
          
        
      The <b>GraphCreationPreRender</b> method is called by Windows Media Player before a file is rendered.


## -parameters




### -param pFilterGraph [in]

Pointer to the <b>IUnknown</b> interface of the Windows Media Player control's DirectShow filter graph.


### -param pReserved [in]

Reserved for future use.


## -returns



Return a success <b>HRESULT</b> to allow playback to continue or a failure code to terminate playback.




## -remarks



You can call <b>QueryInterface</b> through <i>pFilterGraph</i> to retrieve the DirectShow filter graph interfaces you require.

There is no guarantee that this method will be invoked for all files.  Only files rendered with DirectShow will cause this method to be invoked and the WMPGC_FLAGS_USE_CUSTOM_GRAPH flag to be honored. CD, DVD, Image, Flash, Windows Media Format SDK, and Media Foundation playback will not invoke this method.


<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/80d6f1f0-10c9-4e60-9bb7-556e340730a8">IWMPGraphCreation Interface</a>
 

 

