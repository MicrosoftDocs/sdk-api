---
UID: NF:recapis.AdviseInkChange
title: AdviseInkChange function
author: windows-driver-content
description: Stops the recognizer from processing ink because a stroke has been added or deleted.
old-location: tablet\adviseinkchange.htm
old-project: tablet
ms.assetid: 326bbbff-4adc-46ae-aab3-626b55fecf0c
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: 326bbbff-4adc-46ae-aab3-626b55fecf0c, AdviseInkChange, AdviseInkChange function [Tablet PC], recapis/AdviseInkChange, tablet.adviseinkchange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps | UWP apps]
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
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	recapis.h
api_name:
-	AdviseInkChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# AdviseInkChange function


## -description



Stops the recognizer from processing ink because a stroke has been added or deleted.




## -parameters




### -param hrc

The handle to the recognizer context.


### -param bNewStroke

<b>TRUE</b> if adding a new stroke. Set to <b>FALSE</b> if strokes were erased, split, merged, extracted, or deleted from the Ink object.


## -returns



This function can return one of these values.

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
Success. This function also returns S_OK if the recognizer does not support this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is an invalid pointer.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
</table>
 




## -remarks



The <b>AdviseInkChange</b> function signals that there will be additional calls to the <a href="https://msdn.microsoft.com/1db3dbef-41bf-4b00-8e6c-07c7c414e595">AddStroke</a> function. This enables any recognition already in progress to stop at any convenient point. Recognition completion is one such point, so <b>AdviseInkChange</b> can safely do nothing.

For example, if you have two threads, one thread may be using <a href="https://msdn.microsoft.com/1db3dbef-41bf-4b00-8e6c-07c7c414e595">AddStroke</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/dn756307">Process</a> with other functions to obtain results. The other thread may be collecting ink, echoing it, and queuing tasks for the first thread. The second thread calls <b>AdviseInkChange</b> to notify the recognizer a change is coming. This enables the first thread to return to the caller sooner than without the call to <b>AdviseInkChange</b>. The first thread can then call the recognizer again with more ink.

If you set the bNewStroke parameter to <b>FALSE</b> because a stroke was modified or deleted, you must also call the <a href="https://msdn.microsoft.com/92446aca-e611-42b2-8b55-2d1c47ccaa5c">ResetContext</a> function, and then call the <a href="https://msdn.microsoft.com/1db3dbef-41bf-4b00-8e6c-07c7c414e595">AddStroke</a> function to add the strokes from the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object to the recognizer context. This is done automatically if you attach the recognizer context to the <b>InkDisp</b> object.



