---
UID: NF:wmpservices.IWMPGraphCreation.GraphCreationPreRender
title: IWMPGraphCreation::GraphCreationPreRender (wmpservices.h)
description: The GraphCreationPreRender method is called by Windows Media Player before a file is rendered.
helpviewer_keywords: ["GraphCreationPreRender","GraphCreationPreRender method [Windows Media Player]","GraphCreationPreRender method [Windows Media Player]","IWMPGraphCreation interface","IWMPGraphCreation interface [Windows Media Player]","GraphCreationPreRender method","IWMPGraphCreation.GraphCreationPreRender","IWMPGraphCreation::GraphCreationPreRender","IWMPGraphCreationGraphCreationPreRenderdeprecated","wmp.iwmpgraphcreation_graphcreationprerender","wmpservices/IWMPGraphCreation::GraphCreationPreRender"]
old-location: wmp\iwmpgraphcreation_graphcreationprerender.htm
tech.root: WMP
ms.assetid: d3375fa9-2ab0-4e82-9196-0b3971a00185
ms.date: 4/26/2023
ms.keywords: GraphCreationPreRender, GraphCreationPreRender method [Windows Media Player], GraphCreationPreRender method [Windows Media Player],IWMPGraphCreation interface, IWMPGraphCreation interface [Windows Media Player],GraphCreationPreRender method, IWMPGraphCreation.GraphCreationPreRender, IWMPGraphCreation::GraphCreationPreRender, IWMPGraphCreationGraphCreationPreRenderdeprecated, wmp.iwmpgraphcreation_graphcreationprerender, wmpservices/IWMPGraphCreation::GraphCreationPreRender
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPGraphCreation::GraphCreationPreRender
 - wmpservices/IWMPGraphCreation::GraphCreationPreRender
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPGraphCreation.GraphCreationPreRender
---

# IWMPGraphCreation::GraphCreationPreRender


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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

<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation">IWMPGraphCreation Interface</a>