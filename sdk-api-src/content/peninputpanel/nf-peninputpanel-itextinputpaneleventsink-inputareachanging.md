---
UID: NF:peninputpanel.ITextInputPanelEventSink.InputAreaChanging
title: ITextInputPanelEventSink::InputAreaChanging
author: windows-sdk-content
description: Occurs when the input area is about to change on the Tablet PC Input Panel.
old-location: tablet\itextinputpaneleventsink_inputareachanging.htm
old-project: tablet
ms.assetid: e5f96798-2428-4acd-9d9a-addfdf14bb84
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: ITextInputPanelEventSink interface [Tablet PC],InputAreaChanging method, ITextInputPanelEventSink.InputAreaChanging, ITextInputPanelEventSink::InputAreaChanging, InputAreaChanging, InputAreaChanging method [Tablet PC], InputAreaChanging method [Tablet PC],ITextInputPanelEventSink interface, e5f96798-2428-4acd-9d9a-addfdf14bb84, peninputpanel/ITextInputPanelEventSink::InputAreaChanging, tablet.itextinputpaneleventsink_inputareachanging
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
tech.root: 
req.typenames: EventMask
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITextInputPanelEventSink.InputAreaChanging
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: ADAM
---

# ITextInputPanelEventSink::InputAreaChanging


## -description



Occurs when the input area is about to change on the Tablet PC Input Panel.




## -parameters




### -param oldInputArea [in]

The current input area as defined by the <a href="https://msdn.microsoft.com/fc262f07-aa73-49c8-a26a-1f0a47f8269a">PanelInputArea Enumeration</a>.


### -param newInputArea [in]

The input area the Input Panel is changing to as defined by the <a href="https://msdn.microsoft.com/fc262f07-aa73-49c8-a26a-1f0a47f8269a">PanelInputArea Enumeration</a>.


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



<a href="https://msdn.microsoft.com/b30eaa39-a1f7-4c50-992f-11030bb175f9">ITextInputPanelEventSink::InputAreaChanged Method</a>
 

 

