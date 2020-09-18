---
UID: NF:comsvcs.IGetAppTrackerData.GetComponentsInProcess
title: IGetAppTrackerData::GetComponentsInProcess (comsvcs.h)
description: Retrieves summary information for all COM+ components hosted in a single process, or for a specified subset of these components.
helpviewer_keywords: ["GetComponentsInProcess","GetComponentsInProcess method [COM+]","GetComponentsInProcess method [COM+]","IGetAppTrackerData interface","IGetAppTrackerData interface [COM+]","GetComponentsInProcess method","IGetAppTrackerData.GetComponentsInProcess","IGetAppTrackerData::GetComponentsInProcess","comsvcs/IGetAppTrackerData::GetComponentsInProcess","cos.igetapptrackerdata_getcomponentsinprocess"]
old-location: cos\igetapptrackerdata_getcomponentsinprocess.htm
tech.root: cos
ms.assetid: 3a7c2aad-c688-4cd3-a58c-b9c32f9bc035
ms.date: 12/05/2018
ms.keywords: GetComponentsInProcess, GetComponentsInProcess method [COM+], GetComponentsInProcess method [COM+],IGetAppTrackerData interface, IGetAppTrackerData interface [COM+],GetComponentsInProcess method, IGetAppTrackerData.GetComponentsInProcess, IGetAppTrackerData::GetComponentsInProcess, comsvcs/IGetAppTrackerData::GetComponentsInProcess, cos.igetapptrackerdata_getcomponentsinprocess
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
 - IGetAppTrackerData::GetComponentsInProcess
 - comsvcs/IGetAppTrackerData::GetComponentsInProcess
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
 - IGetAppTrackerData.GetComponentsInProcess
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

A combination of flags from the <a href="/windows/desktop/api/comsvcs/ne-comsvcs-getapptrackerdataflags">GetAppTrackerDataFlags</a> enumeration to filter results and to select which data is returned. The following flags are supported: GATD_INCLUDE_LIBRARY_APPS, GATD_INCLUDE_SWC, GATD_INCLUDE_CLASS_NAME, GATD_INCLUDE_APPLICATION_NAME. See Remarks below for more information.

### -param NumComponentsInProcess [out]

On return, the number of components in the process that match the filter criteria specified by <i>PartitionId</i>, <i>ApplicationId</i>, and <i>Flags</i>.

### -param Components [out]

On return, an array of <a href="/windows/desktop/api/comsvcs/ns-comsvcs-componentsummary">ComponentSummary</a> structures for the matching components.

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

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a>