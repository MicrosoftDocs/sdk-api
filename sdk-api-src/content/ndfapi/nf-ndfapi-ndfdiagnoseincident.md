---
UID: NF:ndfapi.NdfDiagnoseIncident
title: NdfDiagnoseIncident function (ndfapi.h)
description: Diagnoses the root cause of an incident without displaying a user interface.
helpviewer_keywords: ["NDF_ADD_CAPTURE_TRACE","NDF_APPLY_INCLUSION_LIST_FILTER","NdfDiagnoseIncident","NdfDiagnoseIncident function [NDF]","ndf.ndfdiagnoseincident","ndfapi/NdfDiagnoseIncident"]
old-location: ndf\ndfdiagnoseincident.htm
tech.root: NDF
ms.assetid: 69ae5624-7c3b-44a2-8468-d587739fc666
ms.date: 12/05/2018
ms.keywords: NDF_ADD_CAPTURE_TRACE, NDF_APPLY_INCLUSION_LIST_FILTER, NdfDiagnoseIncident, NdfDiagnoseIncident function [NDF], ndf.ndfdiagnoseincident, ndfapi/NdfDiagnoseIncident
req.header: ndfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ndfapi.lib
req.dll: Ndfapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NdfDiagnoseIncident
 - ndfapi/NdfDiagnoseIncident
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-net-nfdapi-l1-1-1.dll
 - Ndfapi.dll
api_name:
 - NdfDiagnoseIncident
---

# NdfDiagnoseIncident function


## -description

The <b>NdfDiagnoseIncident</b> function diagnoses the root cause of an incident  without displaying a user interface.

## -parameters

### -param Handle [in]

Type: <b>NDFHANDLE</b>

A handle to the Network Diagnostics Framework incident.

### -param RootCauseCount [out]

Type: <b>ULONG*</b>

The number of root causes that could potentially have caused this incident. If diagnosis does not succeed, the contents of this parameter should be ignored.

### -param RootCauses [out]

Type: <b><a href="/windows/desktop/api/ndattrib/ns-ndattrib-rootcauseinfo">RootCauseInfo</a>**</b>

A collection of <a href="/windows/desktop/api/ndattrib/ns-ndattrib-rootcauseinfo">RootCauseInfo</a> structures that contain a detailed description of the root cause. If diagnosis succeeds, this parameter contains both the leaf root causes identified in the diagnosis session and any non-leaf root causes that have an available repair. If diagnosis does not succeed, the contents of this parameter should be ignored.

Memory allocated to these structures should later be freed.  For an example of how to do this, see the Microsoft Windows Network Diagnostics Samples.

### -param dwWait

Type: <b>DWORD</b>

The length of time, in milliseconds, to wait before terminating the diagnostic routine. INFINITE may be passed to this parameter if no time-out is desired.

### -param dwFlags

Type: <b>DWORD</b>

Possible values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDF_ADD_CAPTURE_TRACE"></a><a id="ndf_add_capture_trace"></a><dl>
<dt><b>NDF_ADD_CAPTURE_TRACE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Turns on network tracing during diagnosis. Diagnostic results will be included in the Event Trace Log (ETL) file returned by <a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfgettracefile">NdfGetTraceFile</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="NDF_APPLY_INCLUSION_LIST_FILTER_"></a><a id="ndf_apply_inclusion_list_filter_"></a><dl>
<dt><b>NDF_APPLY_INCLUSION_LIST_FILTER </b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Applies filtering to the returned root causes so that they are consistent with the in-box scripted diagnostics behavior. Without this flag, root causes will not be filtered. This flag must be set by the caller, so existing callers will not see a change in behavior unless they explicitly specify this flag.

<div class="alert"><b>Note</b>  Available only in Windows 8 and Windows Server 2012.</div>
<div> </div>
</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

Possible return values include, but are not limited to, the following.

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
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The NDF incident handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The diagnostic routine has terminated because it has taken longer than the time-out specified in dwWait.

</td>
</tr>
</table>

## -remarks

This function is intended for use with scenarios where no user interface is shown, or where the standard Windows experience is not being used (as with Media Center and  embedded applications). <a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfexecutediagnosis">NdfExecuteDiagnosis</a> will launch the diagnostics user interface, and should be used in scenarios using the standard Windows experience. You can call either <b>NdfExecuteDiagnosis</b> or <b>NdfDiagnoseIncident</b>, but not both.

Before using this API, an application must call an incident creation function such as <a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfcreatewebincident">NdfCreateWebIncident</a> to begin the NDF diagnostics process. The application then calls <b>NdfDiagnoseIncident</b> to diagnose the issue. If the diagnostics process identifies some possible repairs, the application can call <a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfrepairincident">NdfRepairIncident</a> to repair the problem without displaying a user interface. <a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfcancelincident">NdfCancelIncident</a> can optionally be called from a separate thread if the application wants to cancel an ongoing <b>NdfDiagnoseIncident</b> call. Finally, the application calls <a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfcloseincident">NdfCloseIncident</a>.

The following table shows some examples of root causes and their corresponding repairs.<table>
<tr>
<td>Root cause  GUID</td>
<td>Repair GUID</td>
<td>Root cause description</td>
<td>Repair description</td>
</tr>
<tr>
<td>{4DA030B8-86E5-4b6a-A879-2FFF8443B527}</td>
<td>{1296DFF0-D04E-4be1-A512-90F04DDFA3E6}</td>
<td>A network cable is not properly plugged in or may be broken.</td>
<td>Plug an Ethernet cable into this computer.\nAn Ethernet cable looks like a telephone cable but with larger connectors on the ends. Plug this cable into the opening on the back or side of the computer.\nMake sure the other end of the cable is plugged into the router. If that does not help, try using a different cable.</td>
</tr>
<tr>
<td>{60372FD2-AD60-45c2-BD83-6B827FC438DF}</td>
<td>{07d37f7b-fa5e-4443-bda7-ab107b29afb6}</td>
<td>The %InterfaceName% adapter is disabled.</td>
<td>Enable the %FriendlyInterfaceName% adapter.</td>
</tr>
<tr>
<td>{245A9D66-AE9C-4518-A5B4-655752B0A5BD}</td>
<td>{07d37f7b-fa5e-4443-bda7-ab107b29afb9}</td>
<td>%InterfaceName%"" doesn't have a valid IP configuration.</td>
<td>Reset the ""%InterfaceName%"" adapter.\nThis can sometimes resolve an intermittent problem.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfexecutediagnosis">NdfExecuteDiagnosis</a>



<a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfgettracefile">NdfGetTraceFile</a>



<a href="/windows/desktop/api/ndattrib/ns-ndattrib-rootcauseinfo">RootCauseInfo</a>