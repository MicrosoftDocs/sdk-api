---
UID: NS:contentpartner.WMPContextMenuInfo
title: WMPContextMenuInfo (contentpartner.h)
description: The WMPContextMenuInfo structure contains data about a context menu command.
helpviewer_keywords: ["WMPContextMenuInfo","WMPContextMenuInfo structure [Windows Media Player]","contentpartner/WMPContextMenuInfo","wmp.wmpcontextmenuinfo"]
old-location: wmp\wmpcontextmenuinfo.htm
tech.root: WMP
ms.assetid: a37ddbe1-7c66-4060-b93d-bd494cdc4521
ms.date: 4/26/2023
ms.keywords: WMPContextMenuInfo, WMPContextMenuInfo structure [Windows Media Player], contentpartner/WMPContextMenuInfo, wmp.wmpcontextmenuinfo
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
req.typenames: WMPContextMenuInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPContextMenuInfo
 - contentpartner/WMPContextMenuInfo
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
 - WMPContextMenuInfo
---

# WMPContextMenuInfo structure


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMPContextMenuInfo</b> structure contains data about a context menu command.
<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div><div> </div>

## -struct-fields

### -field dwID

The ID of the command.

### -field bstrMenuText

The menu text to display for the command.

### -field bstrHelpText

The help text to display for the command.

## -remarks

This structure is retrieved by a call to <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands">IWMPContentPartner::GetCommands</a>.

## -see-also

<a href="/windows/desktop/WMP/structures-for-type-1-online-stores">Structures for Type 1 Online Stores</a>