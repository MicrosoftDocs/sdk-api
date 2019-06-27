---
UID: NN:comsvcs.IGetAppTrackerData
title: IGetAppTrackerData (comsvcs.h)
author: windows-sdk-content
description: Enables administrative applications to retrieve statistical information about running COM+ applications.
old-location: cos\igetapptrackerdata.htm
tech.root: cossdk
ms.assetid: f2f9c03b-4f57-4087-8fef-5cdccece91d9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IGetAppTrackerData, IGetAppTrackerData interface [COM+], IGetAppTrackerData interface [COM+],described, comsvcs/IGetAppTrackerData, cos.igetapptrackerdata
ms.topic: interface
f1_keywords: 
 - "comsvcs/IGetAppTrackerData"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IGetAppTrackerData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGetAppTrackerData interface


## -description


Enables administrative applications to retrieve statistical information about running COM+ applications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetAppTrackerData</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGetAppTrackerData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGetAppTrackerData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-igetapptrackerdata-getapplicationprocessdetails">GetApplicationProcessDetails</a>
</td>
<td align="left" width="63%">
Retrieves detailed information about a single process hosting COM+ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-igetapptrackerdata-getapplicationprocesses">GetApplicationProcesses</a>
</td>
<td align="left" width="63%">
Retrieves summary information for all processes that are hosting COM+ applications, or for a specified subset of these processes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-igetapptrackerdata-getapplicationsinprocess">GetApplicationsInProcess</a>
</td>
<td align="left" width="63%">
Retrieves summary information for all COM+ applications hosted in a single process, or for a specified subset of these applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-igetapptrackerdata-getcomponentdetails">GetComponentDetails</a>
</td>
<td align="left" width="63%">
Retrieves detailed information about a single COM+ component hosted in a process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-igetapptrackerdata-getcomponentsinprocess">GetComponentsInProcess</a>
</td>
<td align="left" width="63%">
Retrieves summary information for all COM+ components hosted in a single process, or for a specified subset of these components.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-igetapptrackerdata-getsuggestedpollinginterval">GetSuggestedPollingInterval</a>
</td>
<td align="left" width="63%">
Retrieves the minimum interval for polling suggested by the Tracker Server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-igetapptrackerdata-gettrackerdataascollectionobject">GetTrackerDataAsCollectionObject</a>
</td>
<td align="left" width="63%">
Retrieves tracking data for all COM+ applications in the form of a collection object.

</td>
</tr>
</table> 


## -remarks



Applications that use tracker data will usually need to poll the Tracker Server periodically to ensure that this data is up-to-date. For example, an administrative application that displays tracking data to the user would typically want this data to be near as possible to real-time. However, polling too frequently can degrade overall system performance. Also keep in mind that the COM+ applications updating the data do not send updates to the Tracker Server immediately, so even in the best case there will be some delay (typically only a few seconds).

Polling frequency is a global policy that administrators can adjust, if necessary, to balance between freshness of data and performance impact for the particular set of tools in use on the systems they manage. The value returned in PollingIntervalInSeconds is the minimum amount of time that an application should wait after retrieving tracking data before making another call to retrieve the same data. Any application that polls the Tracker Server should call this method and adjust their polling behavior accordingly.

The polling interval is by default equal to the tracking event frequency (three seconds). This value can be adjusted by writing the following DWORD registry value:


<b>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\COM3</b>\<b>TrackingInfoPollingFrequency</b> = <i>minimum polling interval in seconds</i>





