---
UID: NF:peninputpanel.ITextInputPanelRunInfo.IsTipRunning
title: ITextInputPanelRunInfo::IsTipRunning
author: windows-sdk-content
description: Indicates if the Tablet PC Input Panel is running at the time the method is called.
old-location: tablet\itextinputpanelruninfo_istiprunning.htm
old-project: tablet
ms.assetid: 3d82dd05-c03c-4c97-8d41-84a74e3c3a8a
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 3d82dd05-c03c-4c97-8d41-84a74e3c3a8a, ITextInputPanelRunInfo interface [Tablet PC],IsTipRunning method, ITextInputPanelRunInfo.IsTipRunning, ITextInputPanelRunInfo::IsTipRunning, IsTipRunning, IsTipRunning method [Tablet PC], IsTipRunning method [Tablet PC],ITextInputPanelRunInfo interface, peninputpanel/ITextInputPanelRunInfo::IsTipRunning, tablet.itextinputpanelruninfo_istiprunning
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: peninputpanel.h
req.include-header: 
req.redist: 
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
 - ITextInputPanelRunInfo.IsTipRunning
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: ADAM
---

# ITextInputPanelRunInfo::IsTipRunning


## -description



Indicates if the Tablet PC Input Panel is running at the time the method is called.




## -parameters




### -param pfRunning [out]

<b>TRUE</b> if the Input Panel was running, otherwise <b>FALSE</b>.


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
The <i>pfRunning</i> parameter has been set appropriately.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pfRunning</i> parameter was <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9269a94f-c33f-4e25-bab8-be68e6ead63f">ITextInputPanelRunInfo Interface</a>
 

 

