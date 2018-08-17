---
UID: NF:bdaiface.IBDA_UserActivityService.UserActivityDetected
title: IBDA_UserActivityService::UserActivityDetected
author: windows-sdk-content
description: Indicates that a Media Sink Device (MSD) in a Protected Broadcast Driver Architecture (PBDA) media graph has detected user activity and is informing a Media Transfer Device (MTD) of this activity.
old-location: mstv\ibda_useractivityservice_useractivitydetected.htm
old-project: mstv
ms.assetid: 24c5f6af-602d-4e96-9712-5444ffdd4fe6
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_UserActivityService interface [Microsoft TV Technologies],UserActivityDetected method, IBDA_UserActivityService.UserActivityDetected, IBDA_UserActivityService::UserActivityDetected, UserActivityDetected, UserActivityDetected method [Microsoft TV Technologies], UserActivityDetected method [Microsoft TV Technologies],IBDA_UserActivityService interface, bdaiface/IBDA_UserActivityService::UserActivityDetected, mstv.ibda_useractivityservice_useractivitydetected
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_UserActivityService.UserActivityDetected
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_UserActivityService::UserActivityDetected


## -description


Indicates that a Media Sink Device (MSD) in a Protected Broadcast Driver Architecture (PBDA) media graph has detected user activity and is informing a Media Transfer Device (MTD) of this activity. The MSD calls this method only if the current activity interval has elapsed since the the MSD most recently called this method. The <a href="https://msdn.microsoft.com/en-us/library/Dd797935(v=VS.85).aspx">GetUserActivityInterval</a> method sets or obtains the value of the current activity interval. 


## -parameters






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




<a href="https://msdn.microsoft.com/en-us/library/Dd797935(v=VS.85).aspx">GetUserActivityInterval</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd797933(v=VS.85).aspx">IBDA_UserActivityService</a>
 

 

