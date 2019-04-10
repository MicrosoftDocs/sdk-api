---
UID: NF:bdaiface.IBDA_UserActivityService.GetUserActivityInterval
title: IBDA_UserActivityService::GetUserActivityInterval (bdaiface.h)
author: windows-sdk-content
description: Gets the interval that a Media Sink Device (MSD) in a Protected Broadcast Driver Architecture (PBDA) media graph waits before calling the UserActivityDetected method after the MSD detects user activity.
old-location: mstv\ibda_useractivityservice_getuseractivityinterval.htm
tech.root: mstv
ms.assetid: 2ea3504a-a479-4d26-8a6b-0e5bdddf6a21
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetUserActivityInterval, GetUserActivityInterval method [Microsoft TV Technologies], GetUserActivityInterval method [Microsoft TV Technologies],IBDA_UserActivityService interface, IBDA_UserActivityService interface [Microsoft TV Technologies],GetUserActivityInterval method, IBDA_UserActivityService.GetUserActivityInterval, IBDA_UserActivityService::GetUserActivityInterval, bdaiface/IBDA_UserActivityService::GetUserActivityInterval, mstv.ibda_useractivityservice_getuseractivityinterval
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_UserActivityService.GetUserActivityInterval
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_UserActivityService::GetUserActivityInterval


## -description


Gets the interval that a Media Sink Device (MSD) in a Protected Broadcast Driver Architecture (PBDA) media graph waits before  calling the <a href="https://msdn.microsoft.com/en-us/library/Dd797940(v=VS.85).aspx">UserActivityDetected</a> method after the MSD detects user activity. This interval is known as the <i>user activity interval</i>. An MSD must call this method before it calls <b>UserActivityDetected</b> for the first time, but does not need to call this method thereafter while the graph is running.


## -parameters




### -param pdwActivityInterval [out]

Gets the user activity interval, in seconds.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd797933(v=VS.85).aspx">IBDA_UserActivityService</a>
 

 

