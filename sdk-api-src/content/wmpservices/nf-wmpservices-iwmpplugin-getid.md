---
UID: NF:wmpservices.IWMPPlugin.GetID
title: IWMPPlugin::GetID (wmpservices.h)
description: The IWMPPlugin::GetID method returns the class id of the plug-in.
helpviewer_keywords: ["GetID","GetID method [Windows Media Player]","GetID method [Windows Media Player]","IWMPPlugin interface","IWMPPlugin interface [Windows Media Player]","GetID method","IWMPPlugin.GetID","IWMPPlugin::GetID","IWMPPluginGetIDDSP","wmp.iwmpplugin_getid","wmpservices/IWMPPlugin::GetID"]
old-location: wmp\iwmpplugin_getid.htm
tech.root: WMP
ms.assetid: 883b6e19-5d1a-4ad9-882b-953772e8e11a
ms.date: 4/26/2023
ms.keywords: GetID, GetID method [Windows Media Player], GetID method [Windows Media Player],IWMPPlugin interface, IWMPPlugin interface [Windows Media Player],GetID method, IWMPPlugin.GetID, IWMPPlugin::GetID, IWMPPluginGetIDDSP, wmp.iwmpplugin_getid, wmpservices/IWMPPlugin::GetID
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
 - IWMPPlugin::GetID
 - wmpservices/IWMPPlugin::GetID
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
 - IWMPPlugin.GetID
---

# IWMPPlugin::GetID


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPPlugin::GetID</b> method returns the class id of the plug-in.

## -parameters

### -param pGUID [out]

Pointer to a <b>GUID</b> that represents the class id of the plug-in.

## -returns

The method returns an <b>HRESULT</b>.

## -remarks

For more information on the <b>GUID</b> structure, see the Platform SDK.

## -see-also

<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin">IWMPPlugin Interface</a>