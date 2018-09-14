---
UID: NF:peninputpanel.ITextInputPanelEventSink.TextInserting
title: ITextInputPanelEventSink::TextInserting
author: windows-sdk-content
description: Occurs when the Tablet PC Input Panel is about to insert text into the control with input focus. Provides access to the ink the user entered in the Input Panel.
old-location: tablet\itextinputpaneleventsink_textinserting.htm
tech.root: tablet
ms.assetid: 8e2ca5e2-a407-44cd-b489-c118401ca21b
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: 8e2ca5e2-a407-44cd-b489-c118401ca21b, ITextInputPanelEventSink interface [Tablet PC],TextInserting method, ITextInputPanelEventSink.TextInserting, ITextInputPanelEventSink::TextInserting, TextInserting, TextInserting method [Tablet PC], TextInserting method [Tablet PC],ITextInputPanelEventSink interface, peninputpanel/ITextInputPanelEventSink::TextInserting, tablet.itextinputpaneleventsink_textinserting
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
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITextInputPanelEventSink.TextInserting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextInputPanelEventSink::TextInserting


## -description



Occurs when the Tablet PC Input Panel is about to insert text into the control with input focus. Provides access to the ink the user entered in the Input Panel.




## -parameters




### -param Ink [in]

Array of <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">Ink</a> objects in the Input Panel.


#### - InkObjects [in]

The number of <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">Ink</a> objects in the Ink array parameter.


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
 




## -remarks



There is a minimum of one <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">Ink</a> object for each line of the Input Panel containing text at the time of insertion.




## -see-also




<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a>



<a href="https://msdn.microsoft.com/e3ef6d65-ca6b-4587-bb21-3d3803a3432a">ITextInputPanelEventSink</a>



<a href="https://msdn.microsoft.com/61f3c21f-8658-421b-8494-d39a2faacc66">ITextInputPanelEventSink::TextInserted Method</a>
 

 

