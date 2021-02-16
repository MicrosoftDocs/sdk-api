---
UID: NF:wmp.IWMPEvents.KeyPress
title: IWMPEvents::KeyPress (wmp.h)
description: The KeyPress event occurs when a key is pressed and then released.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","KeyPress method","IWMPEvents.KeyPress","IWMPEvents::KeyPress","IWMPEventsKeyPress","KeyPress","KeyPress method [Windows Media Player]","KeyPress method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__keypress","wmp/IWMPEvents::KeyPress"]
old-location: wmp\iwmpevents_iwmpevents__keypress.htm
tech.root: WMP
ms.assetid: 72d97c04-6978-4275-9adf-2deeebb34224
ms.date: 12/05/2018
ms.keywords: IWMPEvents interface [Windows Media Player],KeyPress method, IWMPEvents.KeyPress, IWMPEvents::KeyPress, IWMPEventsKeyPress, KeyPress, KeyPress method [Windows Media Player], KeyPress method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__keypress, wmp/IWMPEvents::KeyPress
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
 - IWMPEvents::KeyPress
 - wmp/IWMPEvents::KeyPress
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
 - IWMPEvents.KeyPress
---

# IWMPEvents::KeyPress


## -description

The <b>KeyPress</b> event occurs when a key is pressed and then released.

## -parameters

### -param nKeyAscii [in]

Specifies the standard numeric ANSI code for the character.

## -remarks

This event occurs when the keystroke results in any printable keyboard character, the CTRL key combined with a character from the standard alphabet or one of a few special characters, and the ENTER or BACKSPACE key.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>