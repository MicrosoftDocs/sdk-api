---
UID: NF:rtmv2.RtmMarkDestForChangeNotification
title: RtmMarkDestForChangeNotification function
author: windows-sdk-content
description: The RtmMarkDestForChangeNotification function marks a destination for a client.
old-location: rras\rtmmarkdestforchangenotification.htm
tech.root: rras
ms.assetid: b7db8664-2775-4f96-8e5b-5062a8abcfe0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RtmMarkDestForChangeNotification, RtmMarkDestForChangeNotification function [RAS], _rtmv2ref_rtmmarkdestforchangenotification, rras.rtmmarkdestforchangenotification, rtmv2/RtmMarkDestForChangeNotification
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
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmMarkDestForChangeNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmMarkDestForChangeNotification function


## -description


The 
<b>RtmMarkDestForChangeNotification</b> function marks a destination for a client. A marked destination indicates to the routing table manager that it should send the client change notification messages for the marked destination. The client receives change notification messages when a destination changes. The change notifications inform the client of changes to best-route information for the specified destination. This function should be used when 
<a href="https://msdn.microsoft.com/b6e04984-ac92-44a2-a18c-018c6b1b49a9">RtmRegisterForChangeNotification</a> is called to request changes for specific destinations (RTM_NOTIFY_ONLY_MARKED_DESTS).


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param NotifyHandle [in]

Handle to a change notification obtained via a previous call to 
<a href="https://msdn.microsoft.com/b6e04984-ac92-44a2-a18c-018c6b1b49a9">RtmRegisterForChangeNotification</a>.


### -param DestHandle [in]

Handle to the destination that the client is marking for notification of changes.


### -param MarkDest [in]

Specifies whether to mark a destination and receive change notifications. Specify <b>TRUE</b> to mark a destination and start receive change notifications for the specified destination. Specify <b>FALSE</b> to stop receiving change notifications a previously marked destination.


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





## -see-also




<a href="https://msdn.microsoft.com/fafe465a-6c89-45b0-83a9-f08d1d9546c6">RtmGetChangeStatus</a>



<a href="https://msdn.microsoft.com/2b22927d-a857-4bcb-9d89-6ca156b04ea9">RtmGetChangedDests</a>



<a href="https://msdn.microsoft.com/9e0b4311-deba-45d6-b1c2-a1b661f25d0f">RtmIgnoreChangedDests</a>



<a href="https://msdn.microsoft.com/bde390fe-3ada-48d3-b9aa-b4bb56228eac">RtmIsMarkedForChangeNotification</a>



<a href="https://msdn.microsoft.com/b6e04984-ac92-44a2-a18c-018c6b1b49a9">RtmRegisterForChangeNotification</a>



<a href="https://msdn.microsoft.com/542cb23f-81c2-4b29-b049-ebb5827b1d62">RtmReleaseChangedDests</a>
 

 

