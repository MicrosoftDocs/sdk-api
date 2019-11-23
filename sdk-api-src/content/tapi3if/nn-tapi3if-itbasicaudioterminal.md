---
UID: NN:tapi3if.ITBasicAudioTerminal
title: ITBasicAudioTerminal (tapi3if.h)

description: The ITBasicAudioTerminal interface provides methods that allow an application to control basic sound characteristics of terminal.
old-location: tapi3\itbasicaudioterminal.htm
tech.root: Tapi
ms.assetid: 3e676a16-f3ce-433c-9941-8cdccdb01efd

ms.date: 12/05/2018
ms.keywords: ITBasicAudioTerminal, ITBasicAudioTerminal interface [TAPI 2.2], ITBasicAudioTerminal interface [TAPI 2.2],described, _tapi3_itbasicaudioterminal, tapi3.itbasicaudioterminal, tapi3if/ITBasicAudioTerminal
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITBasicAudioTerminal"
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
 - ITBasicAudioTerminal
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITBasicAudioTerminal interface


## -description


The 
<b>ITBasicAudioTerminal</b> interface provides methods that allow an application to control basic sound characteristics of terminal. These methods are taken from the <b>IBasicAudio</b> interface in DirectShow. Please check the index for the Platform Software Development Kit (SDK) for additional information.

The 
<b>ITBasicAudioTerminal</b> interface can be obtained through <b>QueryInterface</b> from terminal objects that support this interface. For example, if the computer running Windows 2000 has a sound card, the addresses exposed by the H323 and IPCONF providers will enumerate, in their 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport">ITTerminalSupport</a> interface, two static terminals that support the 
<b>ITBasicAudioTerminal</b> interface: one for "audio record" and one for "audio playback."


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITBasicAudioTerminal</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITBasicAudioTerminal</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITBasicAudioTerminal</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance">get_Balance</a>
</td>
<td align="left" width="63%">
Gets the balance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_volume">get_Volume</a>
</td>
<td align="left" width="63%">
Gets the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance">put_Balance</a>
</td>
<td align="left" width="63%">
Sets the balance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_volume">put_Volume</a>
</td>
<td align="left" width="63%">
Sets the volume.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/terminal-object">Terminal Object</a>
 

 

