---
UID: NF:rtmv2.RtmGetChangeStatus
title: RtmGetChangeStatus function (rtmv2.h)
description: The RtmGetChangeStatus function checks whether there are pending changes that have not been retrieved with RtmGetChangedDests.
helpviewer_keywords: ["RtmGetChangeStatus","RtmGetChangeStatus function [RAS]","_rtmv2ref_rtmgetchangestatus","rras.rtmgetchangestatus","rtmv2/RtmGetChangeStatus"]
old-location: rras\rtmgetchangestatus.htm
tech.root: RRAS
ms.assetid: fafe465a-6c89-45b0-83a9-f08d1d9546c6
ms.date: 12/05/2018
ms.keywords: RtmGetChangeStatus, RtmGetChangeStatus function [RAS], _rtmv2ref_rtmgetchangestatus, rras.rtmgetchangestatus, rtmv2/RtmGetChangeStatus
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtmGetChangeStatus
 - rtmv2/RtmGetChangeStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmGetChangeStatus
---

# RtmGetChangeStatus function


## -description

The 
<b>RtmGetChangeStatus</b> function checks whether there are pending changes that have not been retrieved with 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangeddests">RtmGetChangedDests</a>.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

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

<a href="/windows/win32/api/rtmv2/nc-rtmv2-_event_callback">RTM_EVENT_CALLBACK</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangeddests">RtmGetChangedDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmignorechangeddests">RtmIgnoreChangedDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmismarkedforchangenotification">RtmIsMarkedForChangeNotification</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmmarkdestforchangenotification">RtmMarkDestForChangeNotification</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasechangeddests">RtmReleaseChangedDests</a>