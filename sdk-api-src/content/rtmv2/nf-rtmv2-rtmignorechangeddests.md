---
UID: NF:rtmv2.RtmIgnoreChangedDests
title: RtmIgnoreChangedDests function
author: windows-sdk-content
description: The RtmIgnoreChangedDests function skips the next change for each destination if it has already occurred.
old-location: rras\rtmignorechangeddests.htm
tech.root: RRAS
ms.assetid: 9e0b4311-deba-45d6-b1c2-a1b661f25d0f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RtmIgnoreChangedDests, RtmIgnoreChangedDests function [RAS], _rtmv2ref_rtmignorechangeddests, rras.rtmignorechangeddests, rtmv2/RtmIgnoreChangedDests
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
 - RtmIgnoreChangedDests
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmIgnoreChangedDests function


## -description


The 
<b>RtmIgnoreChangedDests</b> function skips the next change for each destination if it has already occurred. This function can be used after 
<a href="https://msdn.microsoft.com/fafe465a-6c89-45b0-83a9-f08d1d9546c6">RtmGetChangeStatus</a> to prevent the routing table manager returning this change in response to a call to 
<a href="https://msdn.microsoft.com/2b22927d-a857-4bcb-9d89-6ca156b04ea9">RtmGetChangedDests</a>.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param NotifyHandle [in]

Handle to a change notification.


### -param NumDests [in]

Specifies the number of destinations in <i>ChangedDests</i>.


### -param ChangedDests [in]

Pointer to an array of <b>RTM_DEST_HANDLE</b> handles that indicate the destinations for which to ignore any pending changes.


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
 




## -remarks



When the destinations are no longer required, release them by calling 
<a href="https://msdn.microsoft.com/542cb23f-81c2-4b29-b049-ebb5827b1d62">RtmReleaseChangedDests</a>.




## -see-also




<a href="https://msdn.microsoft.com/fafe465a-6c89-45b0-83a9-f08d1d9546c6">RtmGetChangeStatus</a>



<a href="https://msdn.microsoft.com/2b22927d-a857-4bcb-9d89-6ca156b04ea9">RtmGetChangedDests</a>



<a href="https://msdn.microsoft.com/bde390fe-3ada-48d3-b9aa-b4bb56228eac">RtmIsMarkedForChangeNotification</a>



<a href="https://msdn.microsoft.com/b7db8664-2775-4f96-8e5b-5062a8abcfe0">RtmMarkDestForChangeNotification</a>



<a href="https://msdn.microsoft.com/542cb23f-81c2-4b29-b049-ebb5827b1d62">RtmReleaseChangedDests</a>
 

 

