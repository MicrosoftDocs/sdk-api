---
UID: NF:comsvcs.IGetAppTrackerData.GetComponentDetails
title: IGetAppTrackerData::GetComponentDetails (comsvcs.h)
description: Retrieves detailed information about a single COM+ component hosted in a process.
helpviewer_keywords: ["GetComponentDetails","GetComponentDetails method [COM+]","GetComponentDetails method [COM+]","IGetAppTrackerData interface","IGetAppTrackerData interface [COM+]","GetComponentDetails method","IGetAppTrackerData.GetComponentDetails","IGetAppTrackerData::GetComponentDetails","comsvcs/IGetAppTrackerData::GetComponentDetails","cos.igetapptrackerdata_getcomponentdetails"]
old-location: cos\igetapptrackerdata_getcomponentdetails.htm
tech.root: cos
ms.assetid: 89924a6d-e5cf-4262-9707-d2e4a91dd6ce
ms.date: 12/05/2018
ms.keywords: GetComponentDetails, GetComponentDetails method [COM+], GetComponentDetails method [COM+],IGetAppTrackerData interface, IGetAppTrackerData interface [COM+],GetComponentDetails method, IGetAppTrackerData.GetComponentDetails, IGetAppTrackerData::GetComponentDetails, comsvcs/IGetAppTrackerData::GetComponentDetails, cos.igetapptrackerdata_getcomponentdetails
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
 - IGetAppTrackerData::GetComponentDetails
 - comsvcs/IGetAppTrackerData::GetComponentDetails
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
 - IGetAppTrackerData.GetComponentDetails
---

# IGetAppTrackerData::GetComponentDetails


## -description

Retrieves detailed information about a single COM+ component hosted in a process.

## -parameters

### -param ApplicationInstanceId [in]

The application instance GUID that uniquely identifies the tracked process to select, or GUID_NULL if the <i>ProcessId</i> parameter will be used for selection instead.

### -param ProcessId [in]

The process ID that identifies the process to select, or 0 if <i>ApplicationInstanceId</i> will be used for selection instead.

### -param Clsid [in]

The CLSID of the component.

### -param Flags [in]

A combination of flags from the <a href="/windows/desktop/api/comsvcs/ne-comsvcs-getapptrackerdataflags">GetAppTrackerDataFlags</a> enumeration to select which data is returned. The following flags are supported: GATD_INCLUDE_CLASS_NAME (if retrieving a summary), GATD_INCLUDE_APPLICATION_NAME (if retrieving a summary).

### -param Summary [out]

On return, a <a href="/windows/desktop/api/comsvcs/ns-comsvcs-componentsummary">ComponentSummary</a> structure with summary information for the component. This parameter can be <b>NULL</b>.

### -param Statistics [out]

On return, a <a href="/windows/desktop/api/comsvcs/ns-comsvcs-componentstatistics">ComponentStatistics</a> structure with statistics for the component. This parameter can be <b>NULL</b>.

### -param HangMonitorInfo [out]

On return, a <a href="/windows/desktop/api/comsvcs/ns-comsvcs-componenthangmonitorinfo">ComponentHangMonitorInfo</a> structure with hang monitoring configuration for the component. This parameter can be <b>NULL</b>.

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
<tr>
<td width="40%">
<dl>
<dt><b>COMADMIN_E_OBJECT_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The specified component does not exist in the specified process.

</td>
</tr>
</table>

## -remarks

A process may be selected by its application instance ID or its process ID, but not both. Selection by application instance ID is generally preferred, because process IDs may be reused after a process terminates. However, selection by process ID may be useful if you obtain the process ID from some other source, such as a command line argument to your program. 



You may request any or all of the information available for the component by passing non-<b>NULL</b> values for <i>Summary</i>, <i>Statistics</i>, or <i>HangMonitorInfo</i>. At least one of these parameters must be non-<b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a>