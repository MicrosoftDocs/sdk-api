---
UID: NF:rtmv2.RtmIgnoreChangedDests
title: RtmIgnoreChangedDests function (rtmv2.h)
author: windows-sdk-content
description: The RtmIgnoreChangedDests function skips the next change for each destination if it has already occurred.
old-location: rras\rtmignorechangeddests.htm
tech.root: RRAS
ms.assetid: 9e0b4311-deba-45d6-b1c2-a1b661f25d0f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RtmIgnoreChangedDests, RtmIgnoreChangedDests function [RAS], _rtmv2ref_rtmignorechangeddests, rras.rtmignorechangeddests, rtmv2/RtmIgnoreChangedDests
ms.topic: function
f1_keywords: ["rtmv2/RtmIgnoreChangedDests"]
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
ms.custom: 19H1
---

# RtmIgnoreChangedDests function


## -description


The 
<b>RtmIgnoreChangedDests</b> function skips the next change for each destination if it has already occurred. This function can be used after 
<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangestatus">RtmGetChangeStatus</a> to prevent the routing table manager returning this change in response to a call to 
<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangeddests">RtmGetChangedDests</a>.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.


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
<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasechangeddests">RtmReleaseChangedDests</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangestatus">RtmGetChangeStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangeddests">RtmGetChangedDests</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmismarkedforchangenotification">RtmIsMarkedForChangeNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmmarkdestforchangenotification">RtmMarkDestForChangeNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasechangeddests">RtmReleaseChangedDests</a>
 

 

