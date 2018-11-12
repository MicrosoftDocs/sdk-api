---
UID: NF:tapi3if.ITFileTrack.get_ControllingTerminal
title: ITFileTrack::get_ControllingTerminal
author: windows-sdk-content
description: The get_ControllingTerminal method returns the multitrack terminal that controls the current track.
old-location: tapi3\itfiletrack_get_controllingterminal.htm
tech.root: tapi
ms.assetid: a3a2c5e7-0134-4dad-b192-7a6c71dabe54
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITFileTrack interface [TAPI 2.2],get_ControllingTerminal method, ITFileTrack.get_ControllingTerminal, ITFileTrack::get_ControllingTerminal, _tapi3_itfiletrack_get_controllingterminal, get_ControllingTerminal, get_ControllingTerminal method [TAPI 2.2], get_ControllingTerminal method [TAPI 2.2],ITFileTrack interface, tapi3.itfiletrack_get_controllingterminal, tapi3if/ITFileTrack::get_ControllingTerminal
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
 - ITFileTrack.get_ControllingTerminal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITFileTrack::get_ControllingTerminal


## -description


The 
<b>get_ControllingTerminal</b> method returns the multitrack terminal that controls the current track.


## -parameters




### -param ppControllingTerminal [out]

Pointer to the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>interface returned by <b>ITFileTrack::get_ControllingTerminal</b>. The application must call <b>Release</b> on 
<b>ITTerminal</b>to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/590ca1ea-e058-4238-b01c-249fddd3c87d">ITFileTrack</a>



<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>
 

 

