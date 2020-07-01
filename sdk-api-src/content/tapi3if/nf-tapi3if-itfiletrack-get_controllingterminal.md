---
UID: NF:tapi3if.ITFileTrack.get_ControllingTerminal
title: ITFileTrack::get_ControllingTerminal (tapi3if.h)
description: The get_ControllingTerminal method returns the multitrack terminal that controls the current track.
helpviewer_keywords: ["ITFileTrack interface [TAPI 2.2]","get_ControllingTerminal method","ITFileTrack.get_ControllingTerminal","ITFileTrack::get_ControllingTerminal","_tapi3_itfiletrack_get_controllingterminal","get_ControllingTerminal","get_ControllingTerminal method [TAPI 2.2]","get_ControllingTerminal method [TAPI 2.2]","ITFileTrack interface","tapi3.itfiletrack_get_controllingterminal","tapi3if/ITFileTrack::get_ControllingTerminal"]
old-location: tapi3\itfiletrack_get_controllingterminal.htm
tech.root: Tapi
ms.assetid: a3a2c5e7-0134-4dad-b192-7a6c71dabe54
ms.date: 12/05/2018
ms.keywords: ITFileTrack interface [TAPI 2.2],get_ControllingTerminal method, ITFileTrack.get_ControllingTerminal, ITFileTrack::get_ControllingTerminal, _tapi3_itfiletrack_get_controllingterminal, get_ControllingTerminal, get_ControllingTerminal method [TAPI 2.2], get_ControllingTerminal method [TAPI 2.2],ITFileTrack interface, tapi3.itfiletrack_get_controllingterminal, tapi3if/ITFileTrack::get_ControllingTerminal
f1_keywords:
- tapi3if/ITFileTrack.get_ControllingTerminal
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITFileTrack::get_ControllingTerminal


## -description


The 
<b>get_ControllingTerminal</b> method returns the multitrack terminal that controls the current track.


## -parameters




### -param ppControllingTerminal [out]

Pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>interface returned by <b>ITFileTrack::get_ControllingTerminal</b>. The application must call <b>Release</b> on 
<b>ITTerminal</b>to free resources associated with it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack">ITFileTrack</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>
 

 

