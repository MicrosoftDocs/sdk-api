---
UID: NN:wmpservices.IWMPGraphCreation
title: IWMPGraphCreation (wmpservices.h)
description: The IWMPGraphCreation interface provides methods that Windows Media Player calls to enable you to manage the DirectShow filter graph.
helpviewer_keywords: ["IWMPGraphCreation","IWMPGraphCreation interface [Windows Media Player]","IWMPGraphCreation interface [Windows Media Player]","described","IWMPGraphCreationInterface","wmp.iwmpgraphcreation","wmpservices/IWMPGraphCreation"]
old-location: wmp\iwmpgraphcreation.htm
tech.root: WMP
ms.assetid: 80d6f1f0-10c9-4e60-9bb7-556e340730a8
ms.date: 4/26/2023
ms.keywords: IWMPGraphCreation, IWMPGraphCreation interface [Windows Media Player], IWMPGraphCreation interface [Windows Media Player],described, IWMPGraphCreationInterface, wmp.iwmpgraphcreation, wmpservices/IWMPGraphCreation
req.header: wmpservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPGraphCreation
 - wmpservices/IWMPGraphCreation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmpservices.h
api_name:
 - IWMPGraphCreation
---

# IWMPGraphCreation interface


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPGraphCreation</b> interface provides methods that Windows Media Player calls to enable you to manage the DirectShow filter graph. It can be implemented by an application that embeds the Windows Media Player control.

The Windows Media Player control retrieves a pointer to this interface by calling <b>IServiceProvider::QueryService</b>. When you implement <b>IWMPGraphCreation</b>, you must also implement <b>IServiceProvider</b> and return the correct pointer when <b>QueryService</b> is called with IID_IWMPGraphCreation as the value for the second parameter.

This interface is not supported when remoting the Windows Media Player control.

## -inheritance

The <b>IWMPGraphCreation</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPGraphCreation</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/WMP/interfaces">Interfaces</a>
