---
UID: NF:wmp.IWMPEvents.AudioLanguageChange
title: IWMPEvents::AudioLanguageChange (wmp.h)
description: The AudioLanguageChange event occurs when the current audio language changes.
helpviewer_keywords: ["AudioLanguageChange","AudioLanguageChange method [Windows Media Player]","AudioLanguageChange method [Windows Media Player]","IWMPEvents interface","IWMPEvents interface [Windows Media Player]","AudioLanguageChange method","IWMPEvents.AudioLanguageChange","IWMPEvents::AudioLanguageChange","IWMPEventsAudioLanguageChange","wmp.iwmpevents_iwmpevents__audiolanguagechange","wmp/IWMPEvents::AudioLanguageChange"]
old-location: wmp\iwmpevents_iwmpevents__audiolanguagechange.htm
tech.root: WMP
ms.assetid: c1dbe76f-5cc0-4c12-98bb-2586ee8773d5
ms.date: 12/05/2018
ms.keywords: AudioLanguageChange, AudioLanguageChange method [Windows Media Player], AudioLanguageChange method [Windows Media Player],IWMPEvents interface, IWMPEvents interface [Windows Media Player],AudioLanguageChange method, IWMPEvents.AudioLanguageChange, IWMPEvents::AudioLanguageChange, IWMPEventsAudioLanguageChange, wmp.iwmpevents_iwmpevents__audiolanguagechange, wmp/IWMPEvents::AudioLanguageChange
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
 - IWMPEvents::AudioLanguageChange
 - wmp/IWMPEvents::AudioLanguageChange
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
 - IWMPEvents.AudioLanguageChange
---

# IWMPEvents::AudioLanguageChange


## -description

The <b>AudioLanguageChange</b> event occurs when the current audio language changes.

## -parameters

### -param LangID [in]

Specifies the new language identifier.

## -remarks

A <i>LangID</i> uniquely identifies a particular language dialect, called a locale.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>