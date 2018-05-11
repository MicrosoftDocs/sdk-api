---
UID: NF:peninputpanel.ITextInputPanel.Unadvise
title: ITextInputPanel::Unadvise
author: windows-driver-content
description: Terminates an advisory connection previously established through ITextInputPanel::Advise Method.
old-location: tablet\itextinputpanel_unadvise.htm
old-project: tablet
ms.assetid: 8ea2c112-0d57-4da6-89da-5afe57ff2346
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 8ea2c112-0d57-4da6-89da-5afe57ff2346, ITextInputPanel interface [Tablet PC],Unadvise method, ITextInputPanel.Unadvise, ITextInputPanel::Unadvise, Unadvise, Unadvise method [Tablet PC], Unadvise method [Tablet PC],ITextInputPanel interface, peninputpanel/ITextInputPanel::Unadvise, tablet.itextinputpanel_unadvise
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: peninputpanel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EventMask
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tiptsf.dll
api_name:
-	ITextInputPanel.Unadvise
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITextInputPanel::Unadvise


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Terminates an advisory connection previously established through <a href="https://msdn.microsoft.com/4ea32572-84e6-4230-a634-fc83cb86601f">ITextInputPanel::Advise Method</a>.




## -parameters




### -param EventSink [in]

Reference to the sink object currently receiving event notifications from the Input Panel.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a>



<a href="https://msdn.microsoft.com/4ea32572-84e6-4230-a634-fc83cb86601f">ITextInputPanel::Advise Method</a>
 

 

