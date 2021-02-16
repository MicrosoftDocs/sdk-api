---
UID: NF:wmp.IWMPEvents.ModeChange
title: IWMPEvents::ModeChange (wmp.h)
description: The ModeChange event occurs when a mode of the player is changed.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","ModeChange method","IWMPEvents.ModeChange","IWMPEvents::ModeChange","IWMPEventsModeChange","ModeChange","ModeChange method [Windows Media Player]","ModeChange method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__modechange","wmp/IWMPEvents::ModeChange"]
old-location: wmp\iwmpevents_iwmpevents__modechange.htm
tech.root: WMP
ms.assetid: 64761f19-914a-4ab5-aeb9-12c0aefc8113
ms.date: 12/05/2018
ms.keywords: IWMPEvents interface [Windows Media Player],ModeChange method, IWMPEvents.ModeChange, IWMPEvents::ModeChange, IWMPEventsModeChange, ModeChange, ModeChange method [Windows Media Player], ModeChange method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__modechange, wmp/IWMPEvents::ModeChange
req.header: wmp.h
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEvents::ModeChange
 - wmp/IWMPEvents::ModeChange
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
 - IWMPEvents.ModeChange
---

# IWMPEvents::ModeChange


## -description

The <b>ModeChange</b> event occurs when a mode of the player is changed.

## -parameters

### -param ModeName [in]

Specifies the mode that was changed. Contains one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>shuffle</td>
<td>Tracks are played in random order.</td>
</tr>
<tr>
<td>loop</td>
<td>The entire sequence of tracks is played repeatedly.</td>
</tr>
</table>

### -param NewValue [in]

Indicates the new state of the specified mode.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>