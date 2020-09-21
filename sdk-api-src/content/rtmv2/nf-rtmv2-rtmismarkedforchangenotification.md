---
UID: NF:rtmv2.RtmIsMarkedForChangeNotification
title: RtmIsMarkedForChangeNotification function (rtmv2.h)
description: The RtmIsMarkedForChangeNotification function queries the routing table manager to determine if a destination has previously been marked by a call to RtmMarkDestForChangeNotification.
helpviewer_keywords: ["RtmIsMarkedForChangeNotification","RtmIsMarkedForChangeNotification function [RAS]","_rtmv2ref_rtmismarkedforchangenotification","rras.rtmismarkedforchangenotification","rtmv2/RtmIsMarkedForChangeNotification"]
old-location: rras\rtmismarkedforchangenotification.htm
tech.root: RRAS
ms.assetid: bde390fe-3ada-48d3-b9aa-b4bb56228eac
ms.date: 12/05/2018
ms.keywords: RtmIsMarkedForChangeNotification, RtmIsMarkedForChangeNotification function [RAS], _rtmv2ref_rtmismarkedforchangenotification, rras.rtmismarkedforchangenotification, rtmv2/RtmIsMarkedForChangeNotification
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
 - RtmIsMarkedForChangeNotification
 - rtmv2/RtmIsMarkedForChangeNotification
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
 - RtmIsMarkedForChangeNotification
---

# RtmIsMarkedForChangeNotification function


## -description

The 
<b>RtmIsMarkedForChangeNotification</b> function queries the routing table manager to determine if a destination has previously been marked by a call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmmarkdestforchangenotification">RtmMarkDestForChangeNotification</a>.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param NotifyHandle [in]

Handle to a change notification, obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterforchangenotification">RtmRegisterForChangeNotification</a>.

### -param DestHandle [in]

Handle to the destination to check.

### -param DestMarked [out]

Pointer to a <b>BOOL</b> variable that is <b>TRUE</b> if the destination is marked, <b>FALSE</b> if it is not.

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

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangestatus">RtmGetChangeStatus</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangeddests">RtmGetChangedDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmignorechangeddests">RtmIgnoreChangedDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmmarkdestforchangenotification">RtmMarkDestForChangeNotification</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasechangeddests">RtmReleaseChangedDests</a>