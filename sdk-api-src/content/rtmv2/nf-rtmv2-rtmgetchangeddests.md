---
UID: NF:rtmv2.RtmGetChangedDests
title: RtmGetChangedDests function
author: windows-driver-content
description: The RtmGetChangedDests function returns a set of destinations with changed information.
old-location: rras\rtmgetchangeddests.htm
old-project: RRAS
ms.assetid: 2b22927d-a857-4bcb-9d89-6ca156b04ea9
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: RtmGetChangedDests, RtmGetChangedDests function [RAS], _rtmv2ref_rtmgetchangeddests, rras.rtmgetchangeddests, rtmv2/RtmGetChangedDests
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rtmv2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: RTM_EVENT_TYPE, *PRTM_EVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rtm.dll
api_name:
-	RtmGetChangedDests
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RtmGetChangedDests function


## -description


The 
<b>RtmGetChangedDests</b> function returns a set of destinations with changed information.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param NotifyHandle [in]

Handle to a change notification obtained from a previous call to 
<a href="https://msdn.microsoft.com/b6e04984-ac92-44a2-a18c-018c6b1b49a9">RtmRegisterForChangeNotification</a>.


### -param NumDests [in, out]

On input, <i>NumDests</i> is a pointer to a <b>UINT</b> value that specifies the maximum number of destinations that can be received by <i>ChangedDests</i>. 




On output, <i>NumDests</i> receives the actual number of destinations received by <i>ChangedDests</i>.


### -param ChangedDests [out]

On input, <i>ChangedDests</i> is a pointer to an array of 
<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a> structures. 




On output, <i>ChangedDests</i> is filled with the changed destination information.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contains incorrect information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
No more changed destinations to retrieve.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



A client is notified of changes by an 
<a href="https://msdn.microsoft.com/57179cea-d92b-4199-bb61-b34d980532cf">RTM_EVENT_CALLBACK</a>. The 
<b>RTM_EVENT_CALLBACK</b> is only used to notify the client, not deliver the changes. After a change notification is received, the client must call 
<b>RtmGetChangedDests</b> repeatedly to retrieve all the changes.

If two or more changes to the same destination have occurred since the notification, only the latest change is returned.

When a client no longer needs the handles in <i>ChangedDests</i>, the client must use 
<a href="https://msdn.microsoft.com/542cb23f-81c2-4b29-b049-ebb5827b1d62">RtmReleaseChangedDests</a> to release the handles.

For sample code using this function, see 
<a href="https://msdn.microsoft.com/e079c585-6457-4c2c-82bd-e95d233c4aa6">Use the Event Notification Callback</a>.




## -see-also




<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a>



<a href="https://msdn.microsoft.com/57179cea-d92b-4199-bb61-b34d980532cf">RTM_EVENT_CALLBACK</a>



<a href="https://msdn.microsoft.com/fafe465a-6c89-45b0-83a9-f08d1d9546c6">RtmGetChangeStatus</a>



<a href="https://msdn.microsoft.com/9e0b4311-deba-45d6-b1c2-a1b661f25d0f">RtmIgnoreChangedDests</a>



<a href="https://msdn.microsoft.com/bde390fe-3ada-48d3-b9aa-b4bb56228eac">RtmIsMarkedForChangeNotification</a>



<a href="https://msdn.microsoft.com/b7db8664-2775-4f96-8e5b-5062a8abcfe0">RtmMarkDestForChangeNotification</a>



<a href="https://msdn.microsoft.com/542cb23f-81c2-4b29-b049-ebb5827b1d62">RtmReleaseChangedDests</a>
 

 

