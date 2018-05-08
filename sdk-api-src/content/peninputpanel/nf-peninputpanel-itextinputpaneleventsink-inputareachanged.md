---
UID: NF:peninputpanel.ITextInputPanelEventSink.InputAreaChanged
title: ITextInputPanelEventSink::InputAreaChanged
author: windows-driver-content
description: Occurs when the input area has changed on the Tablet PC Input Panel.
old-location: tablet\itextinputpaneleventsink_inputareachanged.htm
old-project: tablet
ms.assetid: b30eaa39-a1f7-4c50-992f-11030bb175f9
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: ITextInputPanelEventSink interface [Tablet PC],InputAreaChanged method, ITextInputPanelEventSink.InputAreaChanged, ITextInputPanelEventSink::InputAreaChanged, InputAreaChanged, InputAreaChanged method [Tablet PC], InputAreaChanged method [Tablet PC],ITextInputPanelEventSink interface, b30eaa39-a1f7-4c50-992f-11030bb175f9, peninputpanel/ITextInputPanelEventSink::InputAreaChanged, tablet.itextinputpaneleventsink_inputareachanged
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
-	ITextInputPanelEventSink.InputAreaChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITextInputPanelEventSink::InputAreaChanged


## -description



Occurs when the input area has changed on the Tablet PC Input Panel.




## -parameters




### -param oldInputArea [in]

The previous input area as defined by the <a href="https://msdn.microsoft.com/fc262f07-aa73-49c8-a26a-1f0a47f8269a">PanelInputArea Enumeration</a>.


### -param newInputArea [in]

The current input area as defined by the <a href="https://msdn.microsoft.com/fc262f07-aa73-49c8-a26a-1f0a47f8269a">PanelInputArea Enumeration</a>.


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



<a href="https://msdn.microsoft.com/e3ef6d65-ca6b-4587-bb21-3d3803a3432a">ITextInputPanelEventSink</a>



<a href="https://msdn.microsoft.com/e5f96798-2428-4acd-9d9a-addfdf14bb84">ITextInputPanelEventSink::InputAreaChanging Method</a>
 

 

