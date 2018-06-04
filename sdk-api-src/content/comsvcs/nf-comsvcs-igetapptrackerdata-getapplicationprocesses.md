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

# IGetAppTrackerData::GetApplicationProcesses


## -description


Retrieves summary information for all processes that are hosting COM+ applications, or for a specified subset of these processes.


## -parameters




### -param PartitionId [in]

A partition ID to filter results, or GUID_NULL for all partitions.


### -param ApplicationId [in]

An application ID to filter results, or GUID_NULL for all applications.


### -param Flags [in]

A combination of flags from the <a href="https://msdn.microsoft.com/7af61221-e876-4b1c-b416-a92817ad7025">GetAppTrackerDataFlags</a> enumeration to filter results and to select which data is returned. The following flags are supported: GATD_INCLUDE_PROCESS_EXE_NAME, GATD_INCLUDE_LIBRARY_APPS, GATD_INCLUDE_SWC. See remarks below for more information.


### -param NumApplicationProcesses [out]

On return, the number of processes that match the filter criteria specified by <i>PartitionId</i>, <i>ApplicationId</i>, and <i>Flags</i>.


### -param ApplicationProcesses [out]

On return, an array of <a href="https://msdn.microsoft.com/2402aca6-4992-4c6e-a6ff-b4cc50c57dde">ApplicationProcessSummary</a> structures for the matching processes.


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
The method completed successfully and the results are in the <i>ApplicationProcesses</i> parameter.

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
</table>
 




## -remarks



The <i>PartitionId</i>, <i>ApplicationId</i>, and <i>Flags</i> parameters can be used to specify filter criteria if the caller only wants information on a subset of tracked processes.



If neither GATD_INCLUDE_LIBRARY_APPS nor GATD_INCLUDE_SWC are set in <i>Flags</i>, the results include COM+ server application instances only. The <i>ApplicationId</i> parameter can be used to select instances of a specific COM+ server application, and the <i>PartitionId</i> parameter for COM+ server applications from a specific partition.

If either GATD_INCLUDE_LIBRARY_APPS or GATD_INCLUDE_SWC are set, the results also include processes that are hosting COM+ library applications or Services Without Components contexts, respectively. In these cases, <i>ApplicationId</i> and <i>PartitionId</i> filter processes based on all applications (of the requested types) that the process is hosting. If a process includes at least one application that matches the criteria, it will be included in the results.

For example, imagine the following COM+ applications are installed:



<ul>
<li>AppX is a server application in PartitionA.
</li>
<li>AppY is a library application in PartitionA.
</li>
<li>AppZ is a server application in PartitionB.
</li>
</ul>
If <i>PartitionId</i> specifies PartitionA, and GATD_INCLUDE_LIBRARY_APPS is set:



<ul>
<li>An instance of AppX will be included.
</li>
<li>A client process that has created components from AppY will be included.
</li>
<li>An instance of AppZ containing no other COM+ components will not be included because AppZ is not in the partition specified by <i>PartitionId</i>.
</li>
<li>However, if there is another instance of AppZ, but which has also created components from AppY, this process will be included even though the server application is not in the partition specified by <i>PartitionId</i>. This process would not be included if GATD_INCLUDE_LIBRARY_APPS was not set.
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f2f9c03b-4f57-4087-8fef-5cdccece91d9">IGetAppTrackerData</a>
 

 

