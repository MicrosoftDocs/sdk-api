---
UID: NN:wmpservices.IWMPPlugin
title: IWMPPlugin (wmpservices.h)
description: The IWMPPlugin interface is implemented by the plug-in. It manages the connection to Windows Media Player.Note  The interface identifier GUID for this interface changed between the beta release and the final release. .
helpviewer_keywords: ["IWMPPlugin","IWMPPlugin interface [Windows Media Player]","IWMPPlugin interface [Windows Media Player]","described","IWMPPluginInterfaceDSP","wmp.iwmpplugin","wmpservices/IWMPPlugin"]
old-location: wmp\iwmpplugin.htm
tech.root: WMP
ms.assetid: e384aa43-72ab-44b7-b6bd-7a29335b5197
ms.date: 4/26/2023
ms.keywords: IWMPPlugin, IWMPPlugin interface [Windows Media Player], IWMPPlugin interface [Windows Media Player],described, IWMPPluginInterfaceDSP, wmp.iwmpplugin, wmpservices/IWMPPlugin
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
 - IWMPPlugin
 - wmpservices/IWMPPlugin
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
 - IWMPPlugin
---

# IWMPPlugin interface


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPPlugin</b> interface is implemented by the plug-in. It manages the connection to Windows Media Player.

<div class="alert"><b>Note</b>  The interface identifier GUID for this interface changed between the beta release and the final release.</div>
<div> </div>

## -inheritance

The <b>IWMPPlugin</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPPlugin</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/WMP/dsp-plug-in-interfaces">DSP Plug-in Interfaces</a>
