---
UID: NF:peninputpanel.IPenInputPanel.CommitPendingInput
title: IPenInputPanel::CommitPendingInput
author: windows-sdk-content
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Sends collected ink to the recognizer and posts the recognition result.
old-location: tablet\peninputpanel_commitpendinginput.htm
tech.root: tablet
ms.assetid: 4dd0f334-174a-495c-b363-149960ae2253
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 4dd0f334-174a-495c-b363-149960ae2253, CommitPendingInput, CommitPendingInput method [Tablet PC], CommitPendingInput method [Tablet PC],IPenInputPanel interface, IPenInputPanel interface [Tablet PC],CommitPendingInput method, IPenInputPanel.CommitPendingInput, IPenInputPanel::CommitPendingInput, peninputpanel/IPenInputPanel::CommitPendingInput, tablet.peninputpanel_commitpendinginput
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IPenInputPanel.CommitPendingInput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPenInputPanel::CommitPendingInput


## -description



Deprecated.  The <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> has been replaced by the <a href="https://msdn.microsoft.com/867f2d6f-e63a-4c02-9370-3848a3b5c40a">Text Input Panel (TIP)</a>.

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



The writing pad sends the collected ink to the recognizer and clears the writing pad. The East Asian multibox sends recognized characters and clears multiboxes. The recognition result is sent to the control to which the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object is attached.

If there is no pending input or the <a href="https://msdn.microsoft.com/536ba874-b9f9-45c9-bf9a-a64679afc861">CurrentPanel</a> property is <a href="https://msdn.microsoft.com/fbf0ecce-0286-4d1b-99ba-9d28fc25da30">Keyboard</a>, <b>CommitPendingInput</b> does nothing. If the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object is inactive, calling this method generates an error.

Starting with Microsoft Windows XP Tablet PC Edition 2005, ink is recognized as the user is entering. Therefore, the <b>CommitPendingInput</b> function sends the already recognized text to the edit control; it does not force recognition to occur.

Starting with Windows XP Tablet PC Edition 2005, if the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object is inactive, <b>CommitPendingInput</b> does not generate an error, it simply returns.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846809(v=VS.85).aspx">IPenInputPanel</a>



<a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a>
 

 

