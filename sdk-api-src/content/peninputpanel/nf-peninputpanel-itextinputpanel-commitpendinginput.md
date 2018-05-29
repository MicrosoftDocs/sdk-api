---
UID: NF:peninputpanel.ITextInputPanel.CommitPendingInput
title: ITextInputPanel::CommitPendingInput
author: windows-sdk-content
description: Sends collected ink to the recognizer and posts the recognition result.
old-location: tablet\itextinputpanel_commitpendinginput.htm
old-project: tablet
ms.assetid: 652df9e7-5bac-4dc7-bd1a-3934a2bdeb94
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: 652df9e7-5bac-4dc7-bd1a-3934a2bdeb94, CommitPendingInput, CommitPendingInput method [Tablet PC], CommitPendingInput method [Tablet PC],ITextInputPanel interface, ITextInputPanel interface [Tablet PC],CommitPendingInput method, ITextInputPanel.CommitPendingInput, ITextInputPanel::CommitPendingInput, peninputpanel/ITextInputPanel::CommitPendingInput, tablet.itextinputpanel_commitpendinginput
ms.prod: windows
ms.technology: windows-sdk
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
-	ITextInputPanel.CommitPendingInput
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITextInputPanel::CommitPendingInput


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Sends collected ink to the recognizer and posts the recognition result.




## -parameters






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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

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
 




## -remarks



The recognition result is sent to the control to which the <a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> object is attached.




## -see-also




<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a>



<a href="https://msdn.microsoft.com/7ec8acd4-fbb9-4801-880b-fe0d5d3fa3c2">ITextInputPanelEventSink::InPlaceVisibilityChanged Method</a>
 

 

