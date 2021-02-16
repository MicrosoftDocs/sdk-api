---
UID: NF:winsatcominterfacei.IWinSATInitiateEvents.WinSATComplete
title: IWinSATInitiateEvents::WinSATComplete (winsatcominterfacei.h)
description: Receives notification when an assessment succeeds, fails, or is canceled.
helpviewer_keywords: ["IWinSATInitiateEvents interface [WinSAT]","WinSATComplete method","IWinSATInitiateEvents.WinSATComplete","IWinSATInitiateEvents::WinSATComplete","WINSAT_ERROR_ACCESS_DENIED","WINSAT_ERROR_ASSESSMENT_INTERFERENCE","WINSAT_ERROR_COMMAND_LINE_INVALID","WINSAT_ERROR_COMPLETED_ERROR","WINSAT_ERROR_WINSAT_ALREADY_RUNNING","WINSAT_ERROR_WINSAT_CANCELED","WINSAT_STATUS_COMPLETED_SUCCESS","WinSATComplete","WinSATComplete method [WinSAT]","WinSATComplete method [WinSAT]","IWinSATInitiateEvents interface","winsat.iwinsatinitiateevents_winsatcomplete","winsatcominterfacei/IWinSATInitiateEvents::WinSATComplete"]
old-location: winsat\iwinsatinitiateevents_winsatcomplete.htm
tech.root: WinSAT
ms.assetid: a7bcd7e6-b8d7-4ec3-84e8-8ccbcd0b4ada
ms.date: 12/05/2018
ms.keywords: IWinSATInitiateEvents interface [WinSAT],WinSATComplete method, IWinSATInitiateEvents.WinSATComplete, IWinSATInitiateEvents::WinSATComplete, WINSAT_ERROR_ACCESS_DENIED, WINSAT_ERROR_ASSESSMENT_INTERFERENCE, WINSAT_ERROR_COMMAND_LINE_INVALID, WINSAT_ERROR_COMPLETED_ERROR, WINSAT_ERROR_WINSAT_ALREADY_RUNNING, WINSAT_ERROR_WINSAT_CANCELED, WINSAT_STATUS_COMPLETED_SUCCESS, WinSATComplete, WinSATComplete method [WinSAT], WinSATComplete method [WinSAT],IWinSATInitiateEvents interface, winsat.iwinsatinitiateevents_winsatcomplete, winsatcominterfacei/IWinSATInitiateEvents::WinSATComplete
req.header: winsatcominterfacei.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Winsatapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWinSATInitiateEvents::WinSATComplete
 - winsatcominterfacei/IWinSATInitiateEvents::WinSATComplete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Winsatapi.dll
api_name:
 - IWinSATInitiateEvents.WinSATComplete
---

# IWinSATInitiateEvents::WinSATComplete


## -description

<p class="CCE_Message">[IWinSATInitiateEvents::WinSATComplete may be altered or unavailable for releases after Windows 8.1.]

Receives notification when an assessment succeeds, fails, or is canceled.

## -parameters

### -param hresult [in]

The return value of the assessment. The following are the possible return values of the assessment.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINSAT_STATUS_COMPLETED_SUCCESS"></a><a id="winsat_status_completed_success"></a><dl>
<dt><b>WINSAT_STATUS_COMPLETED_SUCCESS</b></dt>
<dt>0x40033</dt>
</dl>
</td>
<td width="60%">
The assessment completed successfully.

</td>
</tr>
<tr>
<td width="40%"><a id="WINSAT_ERROR_ASSESSMENT_INTERFERENCE"></a><a id="winsat_error_assessment_interference"></a><dl>
<dt><b>WINSAT_ERROR_ASSESSMENT_INTERFERENCE</b></dt>
<dt>0x80040034</dt>
</dl>
</td>
<td width="60%">
The assessment could not complete due to system activity.

</td>
</tr>
<tr>
<td width="40%"><a id="WINSAT_ERROR_COMPLETED_ERROR"></a><a id="winsat_error_completed_error"></a><dl>
<dt><b>WINSAT_ERROR_COMPLETED_ERROR</b></dt>
<dt>0x80040035</dt>
</dl>
</td>
<td width="60%">
The assessment could not complete due to an internal or system error.

</td>
</tr>
<tr>
<td width="40%"><a id="WINSAT_ERROR_WINSAT_CANCELED"></a><a id="winsat_error_winsat_canceled"></a><dl>
<dt><b>WINSAT_ERROR_WINSAT_CANCELED</b></dt>
<dt>0x80040036</dt>
</dl>
</td>
<td width="60%">
The assessment was canceled.

</td>
</tr>
<tr>
<td width="40%"><a id="WINSAT_ERROR_COMMAND_LINE_INVALID"></a><a id="winsat_error_command_line_invalid"></a><dl>
<dt><b>WINSAT_ERROR_COMMAND_LINE_INVALID</b></dt>
<dt>0x80040037</dt>
</dl>
</td>
<td width="60%">
The command line passed to WinSAT was not valid.

</td>
</tr>
<tr>
<td width="40%"><a id="WINSAT_ERROR_ACCESS_DENIED"></a><a id="winsat_error_access_denied"></a><dl>
<dt><b>WINSAT_ERROR_ACCESS_DENIED</b></dt>
<dt>0x80040038</dt>
</dl>
</td>
<td width="60%">
The user does not have sufficient privileges to run WinSAT. 

</td>
</tr>
<tr>
<td width="40%"><a id="WINSAT_ERROR_WINSAT_ALREADY_RUNNING"></a><a id="winsat_error_winsat_already_running"></a><dl>
<dt><b>WINSAT_ERROR_WINSAT_ALREADY_RUNNING</b></dt>
<dt>0x80040039</dt>
</dl>
</td>
<td width="60%">
Another copy of WinSAT.exe is already running; only one instance of WinSAT.exe can run on the computer at one time.

</td>
</tr>
</table>

### -param strDescription [in]

The description of the completion status. This string is valid during the life of this callback. Copy the string if you need it after the callback returns.

## -returns

This method should return  S_OK; the value is ignored.

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iinitiatewinsatassessment">IInitiateWinSATAssessment</a>



<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iwinsatinitiateevents">IWinSATInitiateEvents</a>



<a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iwinsatinitiateevents-winsatupdate">IWinSATInitiateEvents::WinSATUpdate</a>