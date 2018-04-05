---
UID: NF:wmp.IWMPEvents.AudioLanguageChange
title: IWMPEvents::AudioLanguageChange method
author: windows-driver-content
description: The AudioLanguageChange event occurs when the current audio language changes.
old-location: wmp\iwmpevents_iwmpevents__audiolanguagechange.htm
old-project: WMP
ms.assetid: c1dbe76f-5cc0-4c12-98bb-2586ee8773d5
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: AudioLanguageChange method [Windows Media Player], AudioLanguageChange method [Windows Media Player], IWMPEvents interface, AudioLanguageChange,IWMPEvents.AudioLanguageChange, IWMPEvents, IWMPEvents interface [Windows Media Player], AudioLanguageChange method, IWMPEvents::AudioLanguageChange, IWMPEventsAudioLanguageChange, wmp.iwmpevents_iwmpevents__audiolanguagechange, wmp/IWMPEvents::AudioLanguageChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPEvents.AudioLanguageChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPEvents::AudioLanguageChange method


## -description



The <b>AudioLanguageChange</b> event occurs when the current audio language changes.




## -parameters




### -param LangID [in]

Specifies the new language identifier.


## -returns



This method does not return a value.




## -remarks



A <i>LangID</i> uniquely identifies a particular language dialect, called a locale.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>
 

 

