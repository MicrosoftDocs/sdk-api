---
UID: NF:peninputpanel.ITextInputPanel.Advise
title: ITextInputPanel::Advise method
author: windows-driver-content
description: Establishes an advisory connection between the Tablet PC Input Panel and the specified sink object.
old-location: tablet\itextinputpanel_advise.htm
old-project: tablet
ms.assetid: 4ea32572-84e6-4230-a634-fc83cb86601f
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: 4ea32572-84e6-4230-a634-fc83cb86601f, Advise method [Tablet PC], Advise method [Tablet PC], ITextInputPanel interface, Advise,ITextInputPanel.Advise, ITextInputPanel, ITextInputPanel interface [Tablet PC], Advise method, ITextInputPanel::Advise, peninputpanel/ITextInputPanel::Advise, tablet.itextinputpanel_advise
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
-	ITextInputPanel.Advise
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ITextInputPanel::Advise method


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Establishes an advisory connection between the Tablet PC Input Panel and the specified sink object.




## -parameters




### -param EventSink [in]

Reference to the sink object to receive event notifications from the Input Panel.


### -param EventMask

A bitwise value of the <a href="https://msdn.microsoft.com/83fefdcf-eb5f-4fb6-b107-dc8abce02bb6">EventMask Enumeration</a>, indicating the events of interest.


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




<a href="https://msdn.microsoft.com/83fefdcf-eb5f-4fb6-b107-dc8abce02bb6">EventMask Enumeration</a>



<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a>



<a href="https://msdn.microsoft.com/8ea2c112-0d57-4da6-89da-5afe57ff2346">ITextInputPanel::Unadvise Method</a>
 

 

