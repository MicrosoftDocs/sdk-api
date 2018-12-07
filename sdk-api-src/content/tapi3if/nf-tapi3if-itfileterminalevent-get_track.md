---
UID: NF:tapi3if.ITFileTerminalEvent.get_Track
title: ITFileTerminalEvent::get_Track
author: windows-sdk-content
description: The get_Track method returns the track terminal that generated this event.
old-location: tapi3\itfileterminalevent_get_track.htm
tech.root: tapi
ms.assetid: f860faf3-6ca5-43d3-8d68-487d1b1d29b0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITFileTerminalEvent interface [TAPI 2.2],get_Track method, ITFileTerminalEvent.get_Track, ITFileTerminalEvent::get_Track, _tapi3_itfileterminalevent_get_track, get_Track, get_Track method [TAPI 2.2], get_Track method [TAPI 2.2],ITFileTerminalEvent interface, tapi3.itfileterminalevent_get_track, tapi3if/ITFileTerminalEvent::get_Track
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITFileTerminalEvent.get_Track
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITFileTerminalEvent::get_Track


## -description


The 
<b>get_Track</b> method returns the track terminal that generated this event.


## -parameters




### -param ppTrackTerminal [out]

Pointer to 
<a href="https://msdn.microsoft.com/590ca1ea-e058-4238-b01c-249fddd3c87d">ITFileTrack</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cb6f2869-ec31-49ac-873b-35a0dcd2c8d7">ITFileTerminalEvent</a>
 

 

