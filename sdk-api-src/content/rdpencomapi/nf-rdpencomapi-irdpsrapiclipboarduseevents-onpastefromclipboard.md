---
UID: NF:rdpencomapi.IRDPSRAPIClipboardUseEvents.OnPasteFromClipboard
title: IRDPSRAPIClipboardUseEvents::OnPasteFromClipboard (rdpencomapi.h)
description: This callback is issued when an attempt to copy data from the sharer computer is made.
helpviewer_keywords: ["IRDPSRAPIClipboardUseEvents interface [RDP]","OnPasteFromClipboard method","IRDPSRAPIClipboardUseEvents.OnPasteFromClipboard","IRDPSRAPIClipboardUseEvents::OnPasteFromClipboard","OnPasteFromClipboard","OnPasteFromClipboard method [RDP]","OnPasteFromClipboard method [RDP]","IRDPSRAPIClipboardUseEvents interface","rdp.irdpsrapiclipboarduseevents_onpastefromclipboard","rdpencomapi/IRDPSRAPIClipboardUseEvents::OnPasteFromClipboard"]
old-location: rdp\irdpsrapiclipboarduseevents_onpastefromclipboard.htm
tech.root: rdp
ms.assetid: aa5fccb9-ca7b-4779-a454-f16be8bca72c
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIClipboardUseEvents interface [RDP],OnPasteFromClipboard method, IRDPSRAPIClipboardUseEvents.OnPasteFromClipboard, IRDPSRAPIClipboardUseEvents::OnPasteFromClipboard, OnPasteFromClipboard, OnPasteFromClipboard method [RDP], OnPasteFromClipboard method [RDP],IRDPSRAPIClipboardUseEvents interface, rdp.irdpsrapiclipboarduseevents_onpastefromclipboard, rdpencomapi/IRDPSRAPIClipboardUseEvents::OnPasteFromClipboard
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPIClipboardUseEvents::OnPasteFromClipboard
 - rdpencomapi/IRDPSRAPIClipboardUseEvents::OnPasteFromClipboard
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncomAPI.h
api_name:
 - IRDPSRAPIClipboardUseEvents.OnPasteFromClipboard
---

# IRDPSRAPIClipboardUseEvents::OnPasteFromClipboard


## -description

This callback is issued when an attempt to copy data from the sharer computer is made.

## -parameters

### -param clipboardFormat [in]

A clipboard format identifier. For more information about clipboard formats, see <a href="/windows/desktop/dataxchg/clipboard-formats">Clipboard Formats</a>. For a list of clipboard format identifiers, see <a href="/windows/desktop/dataxchg/standard-clipboard-formats">Standard Clipboard Formats</a>.

### -param pAttendee [in]

A pointer to the <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiattendee">IRDPSRAPIAttendee</a> instance for the attendee who attempted the clipboard copy.

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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiclipboarduseevents">IRDPSRAPIClipboardUseEvents</a>



<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisessionproperties-get_property">Property</a>