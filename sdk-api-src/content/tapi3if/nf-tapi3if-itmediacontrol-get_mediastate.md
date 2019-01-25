---
UID: NF:tapi3if.ITMediaControl.get_MediaState
title: ITMediaControl::get_MediaState
author: windows-sdk-content
description: The get_MediaState method gets the current state of media on the file terminal.
old-location: tapi3\itmediacontrol_get_mediastate.htm
tech.root: Tapi
ms.assetid: d28063cc-12fe-45b1-8f6a-8c2436926e12
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITMediaControl interface [TAPI 2.2],get_MediaState method, ITMediaControl.get_MediaState, ITMediaControl::get_MediaState, _tapi3_itmediacontrol_get_mediastate, get_MediaState, get_MediaState method [TAPI 2.2], get_MediaState method [TAPI 2.2],ITMediaControl interface, tapi3.itmediacontrol_get_mediastate, tapi3if/ITMediaControl::get_MediaState
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
 - ITMediaControl.get_MediaState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITMediaControl::get_MediaState


## -description


The 
<b>get_MediaState</b> method gets the current state of media on the file terminal.


## -parameters




### -param pTerminalMediaState [out]

Pointer to the 
<a href="https://msdn.microsoft.com/9cc07684-9804-41ac-bc25-f37f6ae00280">TERMINAL_MEDIA_STATE</a> descriptor of the current state of the file terminal.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/016166a1-72ac-4ce8-9c86-43cf94b1bdbd">ITMediaControl</a>



<a href="https://msdn.microsoft.com/9cc07684-9804-41ac-bc25-f37f6ae00280">TERMINAL_MEDIA_STATE</a>
 

 

