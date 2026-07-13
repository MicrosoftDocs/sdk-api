---
UID: NF:effects.IWMPEffects2.OnWindowMessage
title: IWMPEffects2::OnWindowMessage (effects.h)
description: The OnWindowMessage method is called by Windows Media Player to pass window messages to a visualization.
helpviewer_keywords: ["IWMPEffects2 interface [Windows Media Player]","OnWindowMessage method","IWMPEffects2.OnWindowMessage","IWMPEffects2::OnWindowMessage","IWMPEffectsOnWindowMessage","OnWindowMessage","OnWindowMessage method [Windows Media Player]","OnWindowMessage method [Windows Media Player]","IWMPEffects2 interface","effects/IWMPEffects2::OnWindowMessage","wmp.iwmpeffects2_onwindowmessage"]
old-location: wmp\iwmpeffects2_onwindowmessage.htm
tech.root: WMP
ms.assetid: c4efdac9-b50f-4448-98f2-efe015527a4e
ms.date: 4/26/2023
ms.keywords: IWMPEffects2 interface [Windows Media Player],OnWindowMessage method, IWMPEffects2.OnWindowMessage, IWMPEffects2::OnWindowMessage, IWMPEffectsOnWindowMessage, OnWindowMessage, OnWindowMessage method [Windows Media Player], OnWindowMessage method [Windows Media Player],IWMPEffects2 interface, effects/IWMPEffects2::OnWindowMessage, wmp.iwmpeffects2_onwindowmessage
req.header: effects.h
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
 - IWMPEffects2::OnWindowMessage
 - effects/IWMPEffects2::OnWindowMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - effects.h
api_name:
 - IWMPEffects2.OnWindowMessage
---

# IWMPEffects2::OnWindowMessage


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>OnWindowMessage</b> method is called by Windows Media Player to pass window messages to a visualization.

## -parameters

### -param msg [in]

<b>UINT</b> that identifies the window message.

### -param WParam [in]

<b>WPARAM</b> specifying a window message parameter.

### -param LParam [in]

<b>LPARAM</b> specifying a window message parameter.

### -param plResultParam [in]

Pointer to an <b>LRESULT</b> specifying the result code for the window message.

## -returns

This method returns an <b>HRESULT</b>.

## -remarks

Your implementation must only return S_OK if it has handled the window message. If it has not handled the window message, it should return S_FALSE. If this method is not implemented, return E_NOTIMPL.

## -see-also

<a href="/windows/desktop/api/effects/nn-effects-iwmpeffects2">IWMPEffects2 Interface</a>