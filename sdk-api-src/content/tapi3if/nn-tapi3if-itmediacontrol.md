---
UID: NN:tapi3if.ITMediaControl
title: ITMediaControl
author: windows-sdk-content
description: The ITMediaControl interface is a generic interface for media file terminals. The interface exposes methods that allow the application to start, stop, or pause current actions, such as a playback.
old-location: tapi3\itmediacontrol.htm
old-project: tapi
ms.assetid: 016166a1-72ac-4ce8-9c86-43cf94b1bdbd
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITMediaControl, ITMediaControl interface [TAPI 2.2], ITMediaControl interface [TAPI 2.2],described, _tapi3_itmediacontrol, tapi3.itmediacontrol, tapi3if/ITMediaControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITMediaControl
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITMediaControl interface


## -description


The 
<b>ITMediaControl</b> interface is a generic interface for media file terminals. The interface exposes methods that allow the application to start, stop, or pause current actions, such as a playback.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITMediaControl</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITMediaControl</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d28063cc-12fe-45b1-8f6a-8c2436926e12">get_MediaState</a>
</td>
<td align="left" width="63%">
Gets the current state of the file terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a>
</td>
<td align="left" width="63%">
Pauses the action, remaining at the current location in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a>
</td>
<td align="left" width="63%">
Starts the action at the current file location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
Stops the current action, and sets the current location to the beginning of the file.

</td>
</tr>
</table> 

