---
UID: NF:wmpservices.IWMPPlugin.AdviseWMPServices
title: IWMPPlugin::AdviseWMPServices (wmpservices.h)
description: The IWMPPlugin::AdviseWMPServices method is implemented by the plug-in.
helpviewer_keywords: ["AdviseWMPServices","AdviseWMPServices method [Windows Media Player]","AdviseWMPServices method [Windows Media Player]","IWMPPlugin interface","IWMPPlugin interface [Windows Media Player]","AdviseWMPServices method","IWMPPlugin.AdviseWMPServices","IWMPPlugin::AdviseWMPServices","IWMPPluginAdviseWMPServicesDSP","wmp.iwmpplugin_advisewmpservices","wmpservices/IWMPPlugin::AdviseWMPServices"]
old-location: wmp\iwmpplugin_advisewmpservices.htm
tech.root: WMP
ms.assetid: 203b9363-1363-48be-8ba6-8b152ae9a92f
ms.date: 4/26/2023
ms.keywords: AdviseWMPServices, AdviseWMPServices method [Windows Media Player], AdviseWMPServices method [Windows Media Player],IWMPPlugin interface, IWMPPlugin interface [Windows Media Player],AdviseWMPServices method, IWMPPlugin.AdviseWMPServices, IWMPPlugin::AdviseWMPServices, IWMPPluginAdviseWMPServicesDSP, wmp.iwmpplugin_advisewmpservices, wmpservices/IWMPPlugin::AdviseWMPServices
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
 - IWMPPlugin::AdviseWMPServices
 - wmpservices/IWMPPlugin::AdviseWMPServices
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
 - IWMPPlugin.AdviseWMPServices
---

# IWMPPlugin::AdviseWMPServices


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPPlugin::AdviseWMPServices</b> method is implemented by the plug-in.

## -parameters

### -param pWMPServices [in]

Pointer to an <b>IWMPServices</b> interface.

## -returns

The method returns an <b>HRESULT</b>.

## -remarks

Windows Media Player calls the <b>AdviseWMPServices</b> method on the plug-in to pass in a pointer that the plug-in can then use to call the <b>IWMPServices</b> interface, which contains methods that provide information about the current state of the stream.

## -see-also

<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin">IWMPPlugin Interface</a>



<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices">IWMPServices Interface</a>