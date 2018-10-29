---
UID: NN:tapi3if.ITStaticAudioTerminal
title: ITStaticAudioTerminal
author: windows-sdk-content
description: The ITStaticAudioTerminal interface is an interface that TAPI 3.1 MSPs must expose on all static audio terminals. The interface defines methods on static audio terminal objects that are needed to support phone devices.
old-location: tapi3\itstaticaudioterminal.htm
tech.root: Tapi
ms.assetid: 154c07b6-c693-469d-819a-f6d2d2afd744
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITStaticAudioTerminal, ITStaticAudioTerminal interface [TAPI 2.2], ITStaticAudioTerminal interface [TAPI 2.2],described, _tapi3_itstaticaudioterminal, tapi3.itstaticaudioterminal, tapi3if/ITStaticAudioTerminal
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
 - ITStaticAudioTerminal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITStaticAudioTerminal interface


## -description


The 
<b>ITStaticAudioTerminal</b> interface is an interface that TAPI 3.1 MSPs must expose on all static audio terminals. The interface defines methods on static audio terminal objects that are needed to support phone devices.

If an MSP's audio terminals are for devices that are not accessible via standard audio APIs, then a 
<a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> on 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>(IID_ITStaticAudioTerminal) should return E_NOINTERFACE, and it will be impossible to associate a USB phone with any of these audio terminals in TAPI 3.1.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITStaticAudioTerminal</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITStaticAudioTerminal</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITStaticAudioTerminal</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbbfbfe0-843b-4baf-b4f5-51a3037c5fd9">get_WaveId</a>
</td>
<td align="left" width="63%">
Gets the wave ID for the audio device used to implement this terminal.

</td>
</tr>
</table> 

