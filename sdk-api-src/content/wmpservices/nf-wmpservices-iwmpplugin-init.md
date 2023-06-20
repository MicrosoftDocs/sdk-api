---
UID: NF:wmpservices.IWMPPlugin.Init
title: IWMPPlugin::Init (wmpservices.h)
description: The IWMPPlugin::Init method is called when Windows Media Player initializes the plug-in.
helpviewer_keywords: ["IWMPPlugin interface [Windows Media Player]","Init method","IWMPPlugin.Init","IWMPPlugin::Init","IWMPPluginInitDSP","Init","Init method [Windows Media Player]","Init method [Windows Media Player]","IWMPPlugin interface","wmp.iwmpplugin_init","wmpservices/IWMPPlugin::Init"]
old-location: wmp\iwmpplugin_init.htm
tech.root: WMP
ms.assetid: 812752d5-4d4b-4d8d-86a7-c7a9daa092e5
ms.date: 4/26/2023
ms.keywords: IWMPPlugin interface [Windows Media Player],Init method, IWMPPlugin.Init, IWMPPlugin::Init, IWMPPluginInitDSP, Init, Init method [Windows Media Player], Init method [Windows Media Player],IWMPPlugin interface, wmp.iwmpplugin_init, wmpservices/IWMPPlugin::Init
req.header: wmpservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
 - IWMPPlugin::Init
 - wmpservices/IWMPPlugin::Init
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
 - IWMPPlugin.Init
---

# IWMPPlugin::Init


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPPlugin::Init</b> method is called when Windows Media Player initializes the plug-in.

## -parameters

### -param dwPlaybackContext [in]

DWORD value that indicates the particular Windows Media Player playback engine to which the plug-in belongs.

## -returns

The method returns an <b>HRESULT</b>.

## -remarks

It is possible at any given time that multiple instances of Windows Media Player could be running in the same process. For instance, multiple Windows Media Player control instances could be embedded in the same browser window, or even in multiple instances of a browser that coexist in the same process. It is also possible that the same instance of Windows Media Player could create multiple playback engines at the same time. The <i>dwPlaybackContext</i> value allows you to determine which instance of the Windows Media Player playback engine contains the plug-in. This is useful if you wish to enable multiple plug-ins to connect to each other.

<b>Init</b> and <b>Shutdown</b> will always be called on the same thread.

## -see-also

<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin">IWMPPlugin Interface</a>