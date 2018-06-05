---
UID: NF:control.IMediaControl.StopWhenReady
title: IMediaControl::StopWhenReady
author: windows-sdk-content
description: The StopWhenReady method pauses the filter graph, allowing filters to queue data, and then stops the filter graph.
old-location: dshow\imediacontrol_stopwhenready.htm
old-project: DirectShow
ms.assetid: 55dd55b1-51f0-4b47-8432-99741eaee8bb
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IMediaControl interface [DirectShow],StopWhenReady method, IMediaControl.StopWhenReady, IMediaControl::StopWhenReady, IMediaControlStopWhenReady, StopWhenReady, StopWhenReady method [DirectShow], StopWhenReady method [DirectShow],IMediaControl interface, control/IMediaControl::StopWhenReady, dshow.imediacontrol_stopwhenready
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: WMPContextMenuInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMediaControl.StopWhenReady
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IMediaControl::StopWhenReady


## -description



The <code>StopWhenReady</code> method pauses the filter graph, allowing filters to queue data, and then stops the filter graph.




## -parameters






## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The graph was still transitioning to the paused state when the method returned.

</td>
</tr>
</table>
 




## -remarks



This method is useful if you want to seek the filter graph while the graph is stopped. As long as the filter graph is stopped, changes in the current position do not repaint the video window with a new frame. Therefore, calling <a href="https://msdn.microsoft.com/aa1369fd-a57a-4246-bb23-969f6ce3cad8">IMediaSeeking::SetPositions</a> does not update the video window. To update the window after the seek operation, call <code>StopWhenReady</code>. This method transitions the graph to a paused state, waits for the pause operation to complete, and then transitions the graph back to stopped. The pause operation queues data in the graph, so that the video renderer receives and displays the new frame.

This method is asynchronous. It waits on a separate thread for the pause to complete. The calling thread does not block, which enables the application to respond to user input. When the method returns, the logical state of the graph is stopped, even before the pause operation completes. If you call the <a href="https://msdn.microsoft.com/653a94ff-6929-41b1-9b94-dccaff0f7ec7">IMediaControl::GetState</a> method at this point, it returns State_Stopped.

If the application issues another state-change command (such as pause, run, or seek) before the pause operation completes, the new command cancels the pending stop command. The pause operation completes, but the graph does not stop.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bce64088-3751-420c-b9de-b9b5f3119198">IMediaControl Interface</a>
 

 

