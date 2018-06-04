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

# IGetAppTrackerData::GetComponentsInProcess


## -description


Retrieves summary information for all COM+ components hosted in a single process, or for a specified subset of these components.


## -parameters




### -param ApplicationInstanceId [in]

The application instance GUID that uniquely identifies the tracked process to select, or GUID_NULL if the <i>ProcessId</i> parameter will be used for selection instead. 


### -param ProcessId [in]

The process ID that identifies the process to select, or 0 if the <i>ApplicationInstanceId</i> parameter will be used for selection instead. 


### -param PartitionId [in]

A partition ID to filter results, or GUID_NULL for all partitions. 


### -param ApplicationId [in]

An application ID to filter results, or GUID_NULL for all applications. 


### -param Flags [in]

A combination of flags from the <a href="https://msdn.microsoft.com/7af61221-e876-4b1c-b416-a92817ad7025">GetAppTrackerDataFlags</a> enumeration to filter results and to select which data is returned. The following flags are supported: GATD_INCLUDE_LIBRARY_APPS, GATD_INCLUDE_SWC, GATD_INCLUDE_CLASS_NAME, GATD_INCLUDE_APPLICATION_NAME. See Remarks below for more information. 


### -param NumComponentsInProcess [out]

On return, the number of components in the process that match the filter criteria specified by <i>PartitionId</i>, <i>ApplicationId</i>, and <i>Flags</i>. 


### -param Components [out]

On return, an array of <a href="https://msdn.microsoft.com/df752c4a-6a8d-4eac-b3dc-1647bf8a8e5a">ComponentSummary</a> structures for the matching components. 


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
The method completed successfully and the results are in the <i>Components</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully, but there were no components the matched the filter criteria.

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

If neither GATD_INCLUDE_LIBRARY_APPS nor GATD_INCLUDE_SWC are set in <i>Flags</i>, only components from the COM+ server application are included in the results. If GATD_INCLUDE_LIBRARY_APPS is set, components from COM+ library applications in the process, if any, are also included. If GATD_INCLUDE_SWC is set, the results will also include entries for Services Without Components contexts.

If <i>ApplicationId</i> is used to specify an application (it is not set to GUID_NULL), the GATD_INCLUDE_LIBRARY_APPS and GATD_INCLUDE_SWC flags are not meaningful, and it is not valid to use them. Components from the specified application will be returned, regardless of the type of that application.




## -see-also




<a href="https://msdn.microsoft.com/f2f9c03b-4f57-4087-8fef-5cdccece91d9">IGetAppTrackerData</a>
 

 

