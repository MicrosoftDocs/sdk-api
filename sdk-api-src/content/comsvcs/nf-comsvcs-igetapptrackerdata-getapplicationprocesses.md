---
UID: NF:comsvcs.IGetAppTrackerData.GetApplicationProcesses
title: IGetAppTrackerData::GetApplicationProcesses (comsvcs.h)
description: Retrieves summary information for all processes that are hosting COM+ applications, or for a specified subset of these processes.
helpviewer_keywords: ["GetApplicationProcesses","GetApplicationProcesses method [COM+]","GetApplicationProcesses method [COM+]","IGetAppTrackerData interface","IGetAppTrackerData interface [COM+]","GetApplicationProcesses method","IGetAppTrackerData.GetApplicationProcesses","IGetAppTrackerData::GetApplicationProcesses","comsvcs/IGetAppTrackerData::GetApplicationProcesses","cos.igetapptrackerdata_getapplicationprocesses"]
old-location: cos\igetapptrackerdata_getapplicationprocesses.htm
tech.root: cos
ms.assetid: ec15db5c-fce6-42c0-a291-635344a7c4fc
ms.date: 12/05/2018
ms.keywords: GetApplicationProcesses, GetApplicationProcesses method [COM+], GetApplicationProcesses method [COM+],IGetAppTrackerData interface, IGetAppTrackerData interface [COM+],GetApplicationProcesses method, IGetAppTrackerData.GetApplicationProcesses, IGetAppTrackerData::GetApplicationProcesses, comsvcs/IGetAppTrackerData::GetApplicationProcesses, cos.igetapptrackerdata_getapplicationprocesses
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
 - IGetAppTrackerData::GetApplicationProcesses
 - comsvcs/IGetAppTrackerData::GetApplicationProcesses
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
 - IGetAppTrackerData.GetApplicationProcesses
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

A combination of flags from the <a href="/windows/desktop/api/comsvcs/ne-comsvcs-getapptrackerdataflags">GetAppTrackerDataFlags</a> enumeration to filter results and to select which data is returned. The following flags are supported: GATD_INCLUDE_PROCESS_EXE_NAME, GATD_INCLUDE_LIBRARY_APPS, GATD_INCLUDE_SWC. See remarks below for more information.

### -param NumApplicationProcesses [out]

On return, the number of processes that match the filter criteria specified by <i>PartitionId</i>, <i>ApplicationId</i>, and <i>Flags</i>.

### -param ApplicationProcesses [out]

On return, an array of <a href="/windows/desktop/api/comsvcs/ns-comsvcs-applicationprocesssummary">ApplicationProcessSummary</a> structures for the matching processes.

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

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a>