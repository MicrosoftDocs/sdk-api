---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IGetAppTrackerData::GetSuggestedPollingInterval


## -description


Retrieves the minimum interval for polling suggested by the Tracker Server.


## -parameters




### -param PollingIntervalInSeconds [out]

The Tracker Server's suggested polling interval, in seconds.


## -returns



This method can return the standard return values E_INVALIDARG and S_OK.




## -remarks



Applications that use tracker data will usually need to poll the Tracker Server periodically to ensure that this data is up-to-date. For example, an administrative application that displays tracking data to the user would typically want this data to be near as possible to real-time. However, polling too frequently can degrade overall system performance. Also keep in mind that the COM+ applications updating the data do not send updates to the Tracker Server immediately, so even in the best case there will be some delay (typically only a few seconds).



Polling frequency is a global policy that administrators can adjust, if necessary, to balance between freshness of data and performance impact for the particular set of tools in use on the systems they manage. The value returned in <i>PollingIntervalInSeconds</i> is the minimum amount of time that an application should wait after retrieving tracking data before making another call to retrieve the same data. Any application that polls the Tracker Server should call this method and adjust their polling behavior accordingly. 

The polling interval is by default equal to the tracking event frequency (three seconds). This value can be adjusted by writing the following REG_DWORD registry value: 



<b>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\COM3</b>\<b>TrackingInfoPollingFrequency</b> = <i>minimum polling interval</i>




## -see-also




<a href="https://msdn.microsoft.com/f2f9c03b-4f57-4087-8fef-5cdccece91d9">IGetAppTrackerData</a>
 

 

