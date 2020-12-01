---
UID: NF:comsvcs.IGetAppTrackerData.GetSuggestedPollingInterval
title: IGetAppTrackerData::GetSuggestedPollingInterval (comsvcs.h)
description: Retrieves the minimum interval for polling suggested by the Tracker Server.
helpviewer_keywords: ["GetSuggestedPollingInterval","GetSuggestedPollingInterval method [COM+]","GetSuggestedPollingInterval method [COM+]","IGetAppTrackerData interface","IGetAppTrackerData interface [COM+]","GetSuggestedPollingInterval method","IGetAppTrackerData.GetSuggestedPollingInterval","IGetAppTrackerData::GetSuggestedPollingInterval","comsvcs/IGetAppTrackerData::GetSuggestedPollingInterval","cos.igetapptrackerdata_getsuggestedpollinginterval"]
old-location: cos\igetapptrackerdata_getsuggestedpollinginterval.htm
tech.root: cos
ms.assetid: fcc65fd3-debf-4b5c-aaf2-3e7234510d35
ms.date: 12/05/2018
ms.keywords: GetSuggestedPollingInterval, GetSuggestedPollingInterval method [COM+], GetSuggestedPollingInterval method [COM+],IGetAppTrackerData interface, IGetAppTrackerData interface [COM+],GetSuggestedPollingInterval method, IGetAppTrackerData.GetSuggestedPollingInterval, IGetAppTrackerData::GetSuggestedPollingInterval, comsvcs/IGetAppTrackerData::GetSuggestedPollingInterval, cos.igetapptrackerdata_getsuggestedpollinginterval
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IGetAppTrackerData::GetSuggestedPollingInterval
 - comsvcs/IGetAppTrackerData::GetSuggestedPollingInterval
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IGetAppTrackerData.GetSuggestedPollingInterval
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



<b>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\COM3</b>&#92;<b>TrackingInfoPollingFrequency</b> = <i>minimum polling interval</i>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a>