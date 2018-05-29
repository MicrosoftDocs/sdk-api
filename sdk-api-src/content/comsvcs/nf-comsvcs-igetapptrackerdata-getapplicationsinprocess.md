---
UID: NF:comsvcs.IGetAppTrackerData.GetApplicationsInProcess
title: IGetAppTrackerData::GetApplicationsInProcess
author: windows-sdk-content
description: Retrieves summary information for all COM+ applications hosted in a single process, or for a specified subset of these applications.
old-location: cos\igetapptrackerdata_getapplicationsinprocess.htm
old-project: cossdk
ms.assetid: c193a00f-9899-4c26-9357-22603bb195d1
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetApplicationsInProcess, GetApplicationsInProcess method [COM+], GetApplicationsInProcess method [COM+],IGetAppTrackerData interface, IGetAppTrackerData interface [COM+],GetApplicationsInProcess method, IGetAppTrackerData.GetApplicationsInProcess, IGetAppTrackerData::GetApplicationsInProcess, comsvcs/IGetAppTrackerData::GetApplicationsInProcess, cos.igetapptrackerdata_getapplicationsinprocess
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IGetAppTrackerData.GetApplicationsInProcess
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGetAppTrackerData::GetApplicationsInProcess


## -description


Retrieves summary information for all COM+ applications hosted in a single process, or for a specified subset of these applications.


## -parameters




### -param ApplicationInstanceId [in]

The application instance GUID that uniquely identifies the tracked process to select, or GUID_NULL if the <i>ProcessId</i> parameter will be used for selection instead.


### -param ProcessId [in]

The process ID that identifies the process to select, or 0 if <i>ApplicationInstanceId</i> will be used for selection instead. 


### -param PartitionId [in]

A partition ID to filter results, or GUID_NULL for all partitions. 


### -param Flags [in]

A combination of flags from the <a href="https://msdn.microsoft.com/7af61221-e876-4b1c-b416-a92817ad7025">GetAppTrackerDataFlags</a> enumeration to filter results and to select which data is returned. The following flags are supported: GATD_INCLUDE_LIBRARY_APPS, GATD_INCLUDE_SWC, GATD_INCLUDE_APPLICATION_NAME. See Remarks below for more information. 


### -param NumApplicationsInProcess [out]

On return, the number of applications in the process that match the filter criteria specified by <i>PartitionId</i> and <i>Flags</i>. 


### -param Applications [out]

On return, an array of <a href="https://msdn.microsoft.com/3291eede-5318-4d97-a969-ce54381f30af">ApplicationSummary</a> structures for the matching applications. 



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
The method completed successfully and the results are in the <i>Applications</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully, but there were no processes the matched the filter criteria.

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

If neither GATD_INCLUDE_LIBRARY_APPS nor GATD_INCLUDE_SWC are set in <i>Flags</i>, only the COM+ server application is included in the results. If GATD_INCLUDE_LIBRARY_APPS is set, COM+ library applications in the process, if any, are also included. If GATD_INCLUDE_SWC is set, and the process is hosting one or more Services Without Components contexts, the results will also include a single pseudo-application entry with a summary of the SWC contexts.




## -see-also




<a href="https://msdn.microsoft.com/f2f9c03b-4f57-4087-8fef-5cdccece91d9">IGetAppTrackerData</a>
 

 

