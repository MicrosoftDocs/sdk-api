---
UID: NC:lpmapi.CBADMITRESULT
title: CBADMITRESULT (lpmapi.h)
description: The cbAdmitResult function is used by LPMs to return results for the LPM_AdmitRsvpMsg request.
helpviewer_keywords: ["CBADMITRESULT","CBADMITRESULT callback function [QOS]","DUP_RESULTS","INV_LPM_HANDLE","INV_REQ_HANDLE","INV_RESULTS","LPM_TIME_OUT","cbAdmitResult","cbAdmitResult callback","cbAdmitResult callback function [QOS]","lpmapi/cbAdmitResult","qos.cbadmitresult"]
old-location: qos\cbadmitresult.htm
tech.root: QOS
ms.assetid: 9040155b-6c6d-4deb-a63a-74e5fc8123ba
ms.date: 12/05/2018
ms.keywords: CBADMITRESULT, CBADMITRESULT callback function [QOS], DUP_RESULTS, INV_LPM_HANDLE, INV_REQ_HANDLE, INV_RESULTS, LPM_TIME_OUT, cbAdmitResult, cbAdmitResult callback, cbAdmitResult callback function [QOS], lpmapi/cbAdmitResult, qos.cbadmitresult
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - CBADMITRESULT
 - lpmapi/CBADMITRESULT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - lpmapi.h
api_name:
 - CBADMITRESULT
---

# CBADMITRESULT callback function


## -description

The 
<i>cbAdmitResult</i> function is used by LPMs to return results for the 
<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_admitrsvpmsg">LPM_AdmitRsvpMsg</a> request. LPMs should only use this function if they have returned LPM_RESULT_DEFER to the 
<i>LPM_AdmitRsvpMsg</i> function call. The PCM will only accept results from this function within the result time limit established by each LPM through the <i>ResultTimeLimit</i> parameter of the 
<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_initialize">LPM_Initialize</a> function.

## -parameters

### -param LpmHandle [in]

Unique handle for the LPM, as supplied in 
<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_initialize">LPM_Initialize</a>. The PCM will ignore any result that is not accompanied by a valid LPM handle.

### -param RequestHandle [in]

Unique handle that distinguishes this request from all other requests. LPMs must pass this handle to the PCM when returning results asynchronously for an individual request by calling 
<i>cbAdmitResult</i>. The <i>RequestHandle</i> parameter becomes invalid once results are returned, requiring each request to get its own unique <i>RequestHandle</i> from the PCM.

### -param ulPcmActionFlags [in]

Policy Control Module action flags.

### -param LpmError [in]

LPM error code. Must be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INV_LPM_HANDLE"></a><a id="inv_lpm_handle"></a><dl>
<dt><b>INV_LPM_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The supplied LPM handle is invalid.

</td>
</tr>
<tr>
<td width="40%"><a id="LPM_TIME_OUT"></a><a id="lpm_time_out"></a><dl>
<dt><b>LPM_TIME_OUT</b></dt>
</dl>
</td>
<td width="60%">
The LPM has returned results after the time limit.

</td>
</tr>
<tr>
<td width="40%"><a id="INV_REQ_HANDLE"></a><a id="inv_req_handle"></a><dl>
<dt><b>INV_REQ_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The supplied request handle is invalid.

</td>
</tr>
<tr>
<td width="40%"><a id="DUP_RESULTS"></a><a id="dup_results"></a><dl>
<dt><b>DUP_RESULTS</b></dt>
</dl>
</td>
<td width="60%">
The LPM has already returned results for this request.

</td>
</tr>
<tr>
<td width="40%"><a id="INV_RESULTS"></a><a id="inv_results"></a><dl>
<dt><b>INV_RESULTS</b></dt>
</dl>
</td>
<td width="60%">
The results supplied are invalid.

</td>
</tr>
</table>

### -param PolicyDecisionsCount [in]

The number of policy decisions provided in <b>pPolicyDecisions</b>.

### -param pPolicyDecisions [in]

Policy decisions, in the form of one or more <b>POLICY_DECISION</b> structures.

## -returns

This callback function does not return a value.

## -remarks

When a request has been rejected, the PCM will call the LPM to instruct it to delete the request's state. The LPM can choose to delete the request's state at any time during the rejection process. If the LPM deletes a request's state shortly after its rejection of the request, the LPM must be prepared to handle subsequent calls (by the PCM, through the 
<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_deletestate">LPM_DeleteState</a> function) to delete the (already deleted) state.

The LPM does not need to maintain state for requests to which it returns LPV_DONT_CARE. However, the LPM must be prepared to handle 
<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_deletestate">LPM_DeleteState</a> requests for this (nonexisting) state.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_admitrsvpmsg">LPM_AdmitRsvpMsg</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_deletestate">LPM_DeleteState</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_initialize">LPM_Initialize</a>
