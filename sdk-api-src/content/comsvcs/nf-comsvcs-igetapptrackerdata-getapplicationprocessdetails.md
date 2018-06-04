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

# IGetAppTrackerData::GetApplicationProcessDetails


## -description


Retrieves detailed information about a single process hosting COM+ applications.


## -parameters




### -param ApplicationInstanceId [in]

The application instance GUID that uniquely identifies the tracked process to select, or GUID_NULL if the <i>ProcessId</i> parameter will be used for selection instead.


### -param ProcessId [in]

The process ID that identifies the process to select, or 0 if the <i>ApplicationInstanceId</i> parameter will be used for selection instead.


### -param Flags [in]

A combination of flags from the <a href="https://msdn.microsoft.com/7af61221-e876-4b1c-b416-a92817ad7025">GetAppTrackerDataFlags</a> enumeration that specify which data is to be returned. The following flags are supported: GATD_INCLUDE_PROCESS_EXE_NAME (if retrieving a summary).


### -param Summary [out, optional]

On return, a <a href="https://msdn.microsoft.com/2402aca6-4992-4c6e-a6ff-b4cc50c57dde">ApplicationProcessSummary</a> structure with summary information for the process. This parameter can be <b>NULL</b>.


### -param Statistics [out, optional]

On return, a <a href="https://msdn.microsoft.com/7ce16cef-baa4-491c-89e7-f6283e1a646f">ApplicationProcessStatistics</a> structure with statistics for the process. This parameter can be <b>NULL</b>.


### -param RecycleInfo [out, optional]

On return, a <a href="https://msdn.microsoft.com/9e00c6a3-b82e-48a2-bec5-c5fbd6960072">ApplicationProcessRecycleInfo</a> structure with recycling details for the process. This parameter can be <b>NULL</b>.


### -param AnyComponentsHangMonitored [out, optional]

On return, indicates whether any components in the process are configured for hang monitoring. This parameter can be <b>NULL</b>.


## -returns



This method can return the standard return values E_INVALIDARG and E_OUTOFMEMORY, as well as the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMADMIN_E_APP_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The specified process does not exist, or is not hosting any tracked COM+ applications.

</td>
</tr>
</table>
 




## -remarks



A process may be selected by its application instance ID or its process ID, but not both. Selection by application instance ID is generally preferred, because process IDs may be reused after a process terminates. However, selection by process ID may be useful if you obtain the process ID from some other source, such as a command line argument to your program.

You may request any or all of the information available for the process by passing non-<b>NULL</b> values for <i>Summary</i>, <i>Statistics</i>, <i>RecycleInfo</i>, or <i>AnyComponentsHangMonitored</i>. At least one of these parameters must be non-<b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/f2f9c03b-4f57-4087-8fef-5cdccece91d9">IGetAppTrackerData</a>
 

 

