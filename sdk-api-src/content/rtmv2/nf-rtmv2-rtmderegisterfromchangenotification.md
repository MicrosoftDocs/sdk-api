---
UID: NF:rtmv2.RtmDeregisterFromChangeNotification
title: RtmDeregisterFromChangeNotification function (rtmv2.h)
description: The RtmDeregisterFromChangeNotification function unregisters a client from change notification and frees all resources allocated to the notification.
helpviewer_keywords: ["RtmDeregisterFromChangeNotification","RtmDeregisterFromChangeNotification function [RAS]","_rtmv2ref_rtmderegisterfromchangenotification","rras.rtmderegisterfromchangenotification","rtmv2/RtmDeregisterFromChangeNotification"]
old-location: rras\rtmderegisterfromchangenotification.htm
tech.root: RRAS
ms.assetid: 489668ce-9226-470d-8306-5ad0546275e7
ms.date: 12/05/2018
ms.keywords: RtmDeregisterFromChangeNotification, RtmDeregisterFromChangeNotification function [RAS], _rtmv2ref_rtmderegisterfromchangenotification, rras.rtmderegisterfromchangenotification, rtmv2/RtmDeregisterFromChangeNotification
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
 - RtmDeregisterFromChangeNotification
 - rtmv2/RtmDeregisterFromChangeNotification
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
 - RtmDeregisterFromChangeNotification
---

# RtmDeregisterFromChangeNotification function


## -description

The 
<b>RtmDeregisterFromChangeNotification</b> function unregisters a client from change notification and frees all resources allocated to the notification.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterforchangenotification">RtmRegisterForChangeNotification</a>.

### -param NotifyHandle [in]

Handle to the change notification to unregister that is obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterforchangenotification">RtmRegisterForChangeNotification</a>.

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

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmmarkdestforchangenotification">RtmMarkDestForChangeNotification</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterforchangenotification">RtmRegisterForChangeNotification</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasechangeddests">RtmReleaseChangedDests</a>