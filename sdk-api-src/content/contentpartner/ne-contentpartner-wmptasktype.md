---
UID: NE:contentpartner.WMPTaskType
title: WMPTaskType (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The WMPTaskType enumeration represents Windows Media Player task panes.
helpviewer_keywords: ["WMPTaskType","WMPTaskType enumeration [Windows Media Player]","contentpartner/WMPTaskType","contentpartner/wmpttBrowse","contentpartner/wmpttBurn","contentpartner/wmpttCurrent","contentpartner/wmpttSync","enumeration [Windows Media Player]","wmp.wmptasktype","wmpttBrowse","wmpttBurn","wmpttCurrent","wmpttSync"]
old-location: wmp\wmptasktype.htm
tech.root: WMP
ms.assetid: 7abc17b1-5ce7-4741-9a6a-d5a444046418
ms.date: 4/26/2023
ms.keywords: WMPTaskType, WMPTaskType enumeration [Windows Media Player], contentpartner/WMPTaskType, contentpartner/wmpttBrowse, contentpartner/wmpttBurn, contentpartner/wmpttCurrent, contentpartner/wmpttSync, enumeration [Windows Media Player], wmp.wmptasktype, wmpttBrowse, wmpttBurn, wmpttCurrent, wmpttSync
req.header: contentpartner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
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
req.typenames: WMPTaskType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPTaskType
 - contentpartner/WMPTaskType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - contentpartner.h
api_name:
 - WMPTaskType
---

# WMPTaskType enumeration


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>WMPTaskType</b> enumeration represents Windows Media Player task panes.

## -enum-fields

### -field wmpttBrowse:1

The <b>Browse</b> task pane.

### -field wmpttSync:2

The <b>Sync</b> task pane.

### -field wmpttBurn:3

The <b>Burn</b> task pane.

### -field wmpttCurrent:4

Other task pane.

## -see-also

<a href="/windows/desktop/WMP/enumerations-for-type-1-online-stores">Enumerations for Type 1 Online Stores</a>
