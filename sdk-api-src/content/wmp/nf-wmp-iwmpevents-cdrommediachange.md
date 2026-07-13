---
UID: NF:wmp.IWMPEvents.CdromMediaChange
title: IWMPEvents::CdromMediaChange (wmp.h)
description: The CdromMediaChange event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.
helpviewer_keywords: ["CdromMediaChange","CdromMediaChange method [Windows Media Player]","CdromMediaChange method [Windows Media Player]","IWMPEvents interface","IWMPEvents interface [Windows Media Player]","CdromMediaChange method","IWMPEvents.CdromMediaChange","IWMPEvents::CdromMediaChange","IWMPEventsCdromMediaChange","wmp.iwmpevents_iwmpevents__cdrommediachange","wmp/IWMPEvents::CdromMediaChange"]
old-location: wmp\iwmpevents_iwmpevents__cdrommediachange.htm
tech.root: WMP
ms.assetid: 019ab066-ae2b-4517-bc1c-d96bb6e8e15e
ms.date: 4/26/2023
ms.keywords: CdromMediaChange, CdromMediaChange method [Windows Media Player], CdromMediaChange method [Windows Media Player],IWMPEvents interface, IWMPEvents interface [Windows Media Player],CdromMediaChange method, IWMPEvents.CdromMediaChange, IWMPEvents::CdromMediaChange, IWMPEventsCdromMediaChange, wmp.iwmpevents_iwmpevents__cdrommediachange, wmp/IWMPEvents::CdromMediaChange
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
 - IWMPEvents::CdromMediaChange
 - wmp/IWMPEvents::CdromMediaChange
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
 - IWMPEvents.CdromMediaChange
---

# IWMPEvents::CdromMediaChange


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>CdromMediaChange</b> event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.

## -parameters

### -param CdromNum [in]

Specifies the index of the CD or DVD drive.

## -remarks

The index of the CD drive corresponds to the index of a <b>Cdrom</b> object in the <b>IWMPCdromCollection</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection">IWMPCdromCollection Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>