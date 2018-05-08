---
UID: NF:rdpencomapi.IRDPSRAPIClipboardUseEvents.OnPasteFromClipboard
title: IRDPSRAPIClipboardUseEvents::OnPasteFromClipboard
author: windows-driver-content
description: This callback is issued when an attempt to copy data from the sharer computer is made.
old-location: rdp\irdpsrapiclipboarduseevents_onpastefromclipboard.htm
old-project: Rdp
ms.assetid: aa5fccb9-ca7b-4779-a454-f16be8bca72c
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: IRDPSRAPIClipboardUseEvents interface [RDP],OnPasteFromClipboard method, IRDPSRAPIClipboardUseEvents.OnPasteFromClipboard, IRDPSRAPIClipboardUseEvents::OnPasteFromClipboard, OnPasteFromClipboard, OnPasteFromClipboard method [RDP], OnPasteFromClipboard method [RDP],IRDPSRAPIClipboardUseEvents interface, rdp.irdpsrapiclipboarduseevents_onpastefromclipboard, rdpencomapi/IRDPSRAPIClipboardUseEvents::OnPasteFromClipboard
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rdpencomapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RdpEncomAPI.h
api_name:
-	IRDPSRAPIClipboardUseEvents.OnPasteFromClipboard
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRDPSRAPIClipboardUseEvents::OnPasteFromClipboard


## -description


This callback is issued when an attempt to copy data from the sharer computer is made.


## -parameters




### -param clipboardFormat [in]

A clipboard format identifier. For more information about clipboard formats, see <a href="https://msdn.microsoft.com/fe42baec-6b00-4816-b379-7f335da8a197">Clipboard Formats</a>. For a list of clipboard format identifiers, see <a href="https://msdn.microsoft.com/f0af4e61-7ef1-4263-b2c5-e4114515124f">Standard Clipboard Formats</a>.


### -param pAttendee [in]

A pointer to the <a href="https://msdn.microsoft.com/e9edd9f2-ccbf-45b2-b71c-e30368435a60">IRDPSRAPIAttendee</a> instance for the attendee who attempted the clipboard copy. 


### -param pRetVal [out, retval]

The return value for this attempt.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>VARIANT_TRUE</dt>
</dl>
</td>
<td width="60%">
The clipboard copy attempt should be allowed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>VARIANT_FALSE</dt>
</dl>
</td>
<td width="60%">
The clipboard copy attempt should not be allowed. 

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/76ea520c-64c2-4096-ab21-9714b98b5dac">IRDPSRAPIClipboardUseEvents</a>



<a href="https://msdn.microsoft.com/01aee262-95c0-4065-8f8c-e21db66f2a8c">Property</a>
 

 

