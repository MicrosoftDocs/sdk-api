---
UID: NF:wmp.IWMPEvents.ModeChange
title: IWMPEvents::ModeChange
author: windows-sdk-content
description: The ModeChange event occurs when a mode of the player is changed.
old-location: wmp\iwmpevents_iwmpevents__modechange.htm
old-project: WMP
ms.assetid: 64761f19-914a-4ab5-aeb9-12c0aefc8113
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPEvents interface [Windows Media Player],ModeChange method, IWMPEvents.ModeChange, IWMPEvents::ModeChange, IWMPEventsModeChange, ModeChange, ModeChange method [Windows Media Player], ModeChange method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__modechange, wmp/IWMPEvents::ModeChange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents.ModeChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>
 

 

