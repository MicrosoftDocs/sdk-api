---
UID: NF:comsvcs.IGetAppTrackerData.GetApplicationProcessDetails
title: IGetAppTrackerData::GetApplicationProcessDetails (comsvcs.h)
description: Retrieves detailed information about a single process hosting COM+ applications.
helpviewer_keywords: ["GetApplicationProcessDetails","GetApplicationProcessDetails method [COM+]","GetApplicationProcessDetails method [COM+]","IGetAppTrackerData interface","IGetAppTrackerData interface [COM+]","GetApplicationProcessDetails method","IGetAppTrackerData.GetApplicationProcessDetails","IGetAppTrackerData::GetApplicationProcessDetails","comsvcs/IGetAppTrackerData::GetApplicationProcessDetails","cos.igetapptrackerdata_getapplicationprocessdetails"]
old-location: cos\igetapptrackerdata_getapplicationprocessdetails.htm
tech.root: cos
ms.assetid: 37be49c6-b23c-4215-8332-07f6d3eea912
ms.date: 12/05/2018
ms.keywords: GetApplicationProcessDetails, GetApplicationProcessDetails method [COM+], GetApplicationProcessDetails method [COM+],IGetAppTrackerData interface, IGetAppTrackerData interface [COM+],GetApplicationProcessDetails method, IGetAppTrackerData.GetApplicationProcessDetails, IGetAppTrackerData::GetApplicationProcessDetails, comsvcs/IGetAppTrackerData::GetApplicationProcessDetails, cos.igetapptrackerdata_getapplicationprocessdetails
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
 - IGetAppTrackerData::GetApplicationProcessDetails
 - comsvcs/IGetAppTrackerData::GetApplicationProcessDetails
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
 - IGetAppTrackerData.GetApplicationProcessDetails
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

A combination of flags from the <a href="/windows/desktop/api/comsvcs/ne-comsvcs-getapptrackerdataflags">GetAppTrackerDataFlags</a> enumeration that specify which data is to be returned. The following flags are supported: GATD_INCLUDE_PROCESS_EXE_NAME (if retrieving a summary).

### -param Summary [out, optional]

On return, a <a href="/windows/desktop/api/comsvcs/ns-comsvcs-applicationprocesssummary">ApplicationProcessSummary</a> structure with summary information for the process. This parameter can be <b>NULL</b>.

### -param Statistics [out, optional]

On return, a <a href="/windows/desktop/api/comsvcs/ns-comsvcs-applicationprocessstatistics">ApplicationProcessStatistics</a> structure with statistics for the process. This parameter can be <b>NULL</b>.

### -param RecycleInfo [out, optional]

On return, a <a href="/windows/desktop/api/comsvcs/ns-comsvcs-applicationprocessrecycleinfo">ApplicationProcessRecycleInfo</a> structure with recycling details for the process. This parameter can be <b>NULL</b>.

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

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a>