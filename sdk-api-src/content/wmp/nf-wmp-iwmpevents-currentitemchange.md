---
UID: NF:wmp.IWMPEvents.CurrentItemChange
title: IWMPEvents::CurrentItemChange (wmp.h)
description: The CurrentItemChange event occurs when the user or the IWMPControls::put_CurrentItem method changes the current item value.
helpviewer_keywords: ["CurrentItemChange","CurrentItemChange method [Windows Media Player]","CurrentItemChange method [Windows Media Player]","IWMPEvents interface","IWMPEvents interface [Windows Media Player]","CurrentItemChange method","IWMPEvents.CurrentItemChange","IWMPEvents::CurrentItemChange","IWMPEventsCurrentItemChange","wmp.iwmpevents_iwmpevents__currentitemchange","wmp/IWMPEvents::CurrentItemChange"]
old-location: wmp\iwmpevents_iwmpevents__currentitemchange.htm
tech.root: WMP
ms.assetid: 3669fe6e-233e-4214-9f84-763a06835f48
ms.date: 4/26/2023
ms.keywords: CurrentItemChange, CurrentItemChange method [Windows Media Player], CurrentItemChange method [Windows Media Player],IWMPEvents interface, IWMPEvents interface [Windows Media Player],CurrentItemChange method, IWMPEvents.CurrentItemChange, IWMPEvents::CurrentItemChange, IWMPEventsCurrentItemChange, wmp.iwmpevents_iwmpevents__currentitemchange, wmp/IWMPEvents::CurrentItemChange
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
 - IWMPEvents::CurrentItemChange
 - wmp/IWMPEvents::CurrentItemChange
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
 - IWMPEvents.CurrentItemChange
---

# IWMPEvents::CurrentItemChange


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>CurrentItemChange</b> event occurs when the user or the <b>IWMPControls::put_CurrentItem</b> method changes the current item value.

## -parameters

### -param pdispMedia [in]

Pointer to an <b>IDispatch</b> interface that identifies the new current item.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-put_currentitem">IWMPControls::put_currentItem</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>