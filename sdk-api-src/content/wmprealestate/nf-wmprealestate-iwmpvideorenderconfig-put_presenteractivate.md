---
UID: NF:wmprealestate.IWMPVideoRenderConfig.put_presenterActivate
title: IWMPVideoRenderConfig::put_presenterActivate (wmprealestate.h)
description: The put_presenterActivate method provides Windows Media Player with an activation object for a custom video presenter.
helpviewer_keywords: ["IWMPVideoRenderConfig interface [Windows Media Player]","put_presenterActivate method","IWMPVideoRenderConfig.put_presenterActivate","IWMPVideoRenderConfig::put_presenterActivate","IWMPVideoRenderConfigput_presenterActivate","put_presenterActivate","put_presenterActivate method [Windows Media Player]","put_presenterActivate method [Windows Media Player]","IWMPVideoRenderConfig interface","wmp.iwmpvideorenderconfig_put_presenteractivate","wmprealestate/IWMPVideoRenderConfig::put_presenterActivate"]
old-location: wmp\iwmpvideorenderconfig_put_presenteractivate.htm
tech.root: WMP
ms.assetid: a052aecc-b37f-4999-b484-80ee3e2392ba
ms.date: 4/26/2023
ms.keywords: IWMPVideoRenderConfig interface [Windows Media Player],put_presenterActivate method, IWMPVideoRenderConfig.put_presenterActivate, IWMPVideoRenderConfig::put_presenterActivate, IWMPVideoRenderConfigput_presenterActivate, put_presenterActivate, put_presenterActivate method [Windows Media Player], put_presenterActivate method [Windows Media Player],IWMPVideoRenderConfig interface, wmp.iwmpvideorenderconfig_put_presenteractivate, wmprealestate/IWMPVideoRenderConfig::put_presenterActivate
req.header: wmprealestate.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
 - IWMPVideoRenderConfig::put_presenterActivate
 - wmprealestate/IWMPVideoRenderConfig::put_presenterActivate
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
 - IWMPVideoRenderConfig.put_presenterActivate
---

# IWMPVideoRenderConfig::put_presenterActivate


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_presenterActivate</b> method provides Windows Media Player with an activation object for a custom video presenter.

## -parameters

### -param pActivate [in]

A pointer to an <b>IMFActivate</b> interface that Windows Media Player or another Windows component will use to activate the custom video presenter.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

In certain situations, Windows Media Player uses a video pipeline that includes the enhanced video renderer (EVR). The EVR is a system component that allows other components and applications to provide custom plug-ins that perform tasks like video mixing and video presenting.

An application that embeds Windows Media Player can provide a custom video presenter for the EVR by calling <b>put_presenterActivate</b>. The application must create its own activation object that implements the <b>IMFActivate</b> interface. The application provides Windows Media Player with that interface in the <i>pActivate</i> parameter. When Windows Media Player or another system component needs to create an instance of the custom presenter, it calls the <b>ActivateObject</b> method of the <b>IMFActivate</b> interface provided by the application.

The activation object is responsible for initializing the custom presenter. The nature of the initialization and the format of any context data required for the initialization are completely under the control of those who develop the custom presenter and the activation object.

The EVR, custom presenters, activation objects, and the <b>IMFActivate</b> interface are documented in the Microsoft Media Foundation SDK, which is part of the Microsoft Windows SDK.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig">IWMPVideoRenderConfig Interface</a>