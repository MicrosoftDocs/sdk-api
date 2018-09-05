---
UID: NF:rtmv2.RtmGetChangeStatus
title: RtmGetChangeStatus function
author: windows-sdk-content
description: The RtmGetChangeStatus function checks whether there are pending changes that have not been retrieved with RtmGetChangedDests.
old-location: rras\rtmgetchangestatus.htm
old-project: RRAS
ms.assetid: fafe465a-6c89-45b0-83a9-f08d1d9546c6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RtmGetChangeStatus, RtmGetChangeStatus function [RAS], _rtmv2ref_rtmgetchangestatus, rras.rtmgetchangestatus, rtmv2/RtmGetChangeStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rtmv2.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RTM_EVENT_TYPE, *PRTM_EVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmGetChangeStatus
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: ADAM
---

# RtmGetChangeStatus function


## -description


The 
<b>RtmGetChangeStatus</b> function checks whether there are pending changes that have not been retrieved with 
<a href="https://msdn.microsoft.com/2b22927d-a857-4bcb-9d89-6ca156b04ea9">RtmGetChangedDests</a>.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param NotifyHandle [in]

Handle to a change notification.


### -param DestHandle [in]

Handle to the destination for which to return change status.


### -param ChangeStatus [out]

On input, <i>ChangeStatus</i> is a pointer to a <b>BOOL</b> value. 




On output, <i>ChangeStatus</i> receives either <b>TRUE</b> or <b>FALSE</b> to indicate if the destination specified by <i>DestHandle</i> has a change notification pending.


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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



This function can be used to make portions of the client code more efficient. For example, a client may postpone some operation if there are changes that the client has not yet processed.

This function can also be used to monitor change notification in another thread.




## -see-also




<a href="https://msdn.microsoft.com/57179cea-d92b-4199-bb61-b34d980532cf">RTM_EVENT_CALLBACK</a>



<a href="https://msdn.microsoft.com/2b22927d-a857-4bcb-9d89-6ca156b04ea9">RtmGetChangedDests</a>



<a href="https://msdn.microsoft.com/9e0b4311-deba-45d6-b1c2-a1b661f25d0f">RtmIgnoreChangedDests</a>



<a href="https://msdn.microsoft.com/bde390fe-3ada-48d3-b9aa-b4bb56228eac">RtmIsMarkedForChangeNotification</a>



<a href="https://msdn.microsoft.com/b7db8664-2775-4f96-8e5b-5062a8abcfe0">RtmMarkDestForChangeNotification</a>



<a href="https://msdn.microsoft.com/542cb23f-81c2-4b29-b049-ebb5827b1d62">RtmReleaseChangedDests</a>
 

 

