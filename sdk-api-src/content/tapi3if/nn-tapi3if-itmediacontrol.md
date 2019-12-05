---
UID: NN:tapi3if.ITMediaControl
title: ITMediaControl (tapi3if.h)
description: The ITMediaControl interface is a generic interface for media file terminals. The interface exposes methods that allow the application to start, stop, or pause current actions, such as a playback.
old-location: tapi3\itmediacontrol.htm
tech.root: Tapi
ms.assetid: 016166a1-72ac-4ce8-9c86-43cf94b1bdbd
ms.date: 12/05/2018
ms.keywords: ITMediaControl, ITMediaControl interface [TAPI 2.2], ITMediaControl interface [TAPI 2.2],described, _tapi3_itmediacontrol, tapi3.itmediacontrol, tapi3if/ITMediaControl
ms.topic: interface
f1_keywords:
- tapi3if/ITMediaControl
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
- ITMediaControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITMediaControl interface


## -description


The 
<b>ITMediaControl</b> interface is a generic interface for media file terminals. The interface exposes methods that allow the application to start, stop, or pause current actions, such as a playback.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITMediaControl</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITMediaControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITMediaControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-get_mediastate">get_MediaState</a>
</td>
<td align="left" width="63%">
Gets the current state of the file terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses the action, remaining at the current location in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start">Start</a>
</td>
<td align="left" width="63%">
Starts the action at the current file location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops the current action, and sets the current location to the beginning of the file.

</td>
</tr>
</table> 

