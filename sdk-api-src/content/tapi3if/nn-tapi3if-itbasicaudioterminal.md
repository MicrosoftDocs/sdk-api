---
UID: NN:tapi3if.ITBasicAudioTerminal
title: ITBasicAudioTerminal
author: windows-sdk-content
description: The ITBasicAudioTerminal interface provides methods that allow an application to control basic sound characteristics of terminal.
old-location: tapi3\itbasicaudioterminal.htm
tech.root: tapi
ms.assetid: 3e676a16-f3ce-433c-9941-8cdccdb01efd
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITBasicAudioTerminal, ITBasicAudioTerminal interface [TAPI 2.2], ITBasicAudioTerminal interface [TAPI 2.2],described, _tapi3_itbasicaudioterminal, tapi3.itbasicaudioterminal, tapi3if/ITBasicAudioTerminal
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITBasicAudioTerminal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITBasicAudioTerminal interface


## -description


The 
<b>ITBasicAudioTerminal</b> interface provides methods that allow an application to control basic sound characteristics of terminal. These methods are taken from the <b>IBasicAudio</b> interface in DirectShow. Please check the index for the Platform Software Development Kit (SDK) for additional information.

The 
<b>ITBasicAudioTerminal</b> interface can be obtained through <b>QueryInterface</b> from terminal objects that support this interface. For example, if the computer running Windows 2000 has a sound card, the addresses exposed by the H323 and IPCONF providers will enumerate, in their 
<a href="https://msdn.microsoft.com/8669324a-5c2c-4ed8-be24-a0c71fbb8c01">ITTerminalSupport</a> interface, two static terminals that support the 
<b>ITBasicAudioTerminal</b> interface: one for "audio record" and one for "audio playback."


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITBasicAudioTerminal</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITBasicAudioTerminal</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/36aff613-6065-4d92-98e7-3e5b851bf544">get_Balance</a>
</td>
<td align="left" width="63%">
Gets the balance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d3a64fa-41b6-44c4-a67e-08113e771cc7">get_Volume</a>
</td>
<td align="left" width="63%">
Gets the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8337376e-5de6-4d6d-9f95-49b83d438168">put_Balance</a>
</td>
<td align="left" width="63%">
Sets the balance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c611505-74b4-48fa-bb36-ec765cb24f96">put_Volume</a>
</td>
<td align="left" width="63%">
Sets the volume.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>
 

 

