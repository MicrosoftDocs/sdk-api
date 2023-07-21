---
UID: NF:bdaiface.IBDA_UserActivityService.UserActivityDetected
title: IBDA_UserActivityService::UserActivityDetected (bdaiface.h)
description: Indicates that a Media Sink Device (MSD) in a Protected Broadcast Driver Architecture (PBDA) media graph has detected user activity and is informing a Media Transfer Device (MTD) of this activity.
helpviewer_keywords: ["IBDA_UserActivityService interface [Microsoft TV Technologies]","UserActivityDetected method","IBDA_UserActivityService.UserActivityDetected","IBDA_UserActivityService::UserActivityDetected","UserActivityDetected","UserActivityDetected method [Microsoft TV Technologies]","UserActivityDetected method [Microsoft TV Technologies]","IBDA_UserActivityService interface","bdaiface/IBDA_UserActivityService::UserActivityDetected","mstv.ibda_useractivityservice_useractivitydetected"]
old-location: mstv\ibda_useractivityservice_useractivitydetected.htm
tech.root: mstv
ms.assetid: 24c5f6af-602d-4e96-9712-5444ffdd4fe6
ms.date: 12/05/2018
ms.keywords: IBDA_UserActivityService interface [Microsoft TV Technologies],UserActivityDetected method, IBDA_UserActivityService.UserActivityDetected, IBDA_UserActivityService::UserActivityDetected, UserActivityDetected, UserActivityDetected method [Microsoft TV Technologies], UserActivityDetected method [Microsoft TV Technologies],IBDA_UserActivityService interface, bdaiface/IBDA_UserActivityService::UserActivityDetected, mstv.ibda_useractivityservice_useractivitydetected
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_UserActivityService::UserActivityDetected
 - bdaiface/IBDA_UserActivityService::UserActivityDetected
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_UserActivityService.UserActivityDetected
---

# IBDA_UserActivityService::UserActivityDetected


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Indicates that a Media Sink Device (MSD) in a Protected Broadcast Driver Architecture (PBDA) media graph has detected user activity and is informing a Media Transfer Device (MTD) of this activity. The MSD calls this method only if the current activity interval has elapsed since the the MSD most recently called this method. The <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_useractivityservice-getuseractivityinterval">GetUserActivityInterval</a> method sets or obtains the value of the current activity interval.



## -returns

This method can return one of these values.

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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
User activity service failed.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_useractivityservice-getuseractivityinterval">GetUserActivityInterval</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_useractivityservice">IBDA_UserActivityService</a>
