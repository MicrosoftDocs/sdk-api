---
UID: NS:pdh._BrowseDlgConfig_HW
title: PDH_BROWSE_DLG_CONFIG_HW (pdh.h)
description: The PDH_BROWSE_DLG_CONFIG_H structure is used by the PdhBrowseCountersH function to configure the Browse Performance Counters dialog box. (Unicode)
helpviewer_keywords: ["*PPDH_BROWSE_DLG_CONFIG_HW","PDH_BROWSE_DLG_CONFIG_H","PDH_BROWSE_DLG_CONFIG_H structure [Perf]","PDH_BROWSE_DLG_CONFIG_HA","PDH_BROWSE_DLG_CONFIG_HW","PERF_DETAIL_ADVANCED","PERF_DETAIL_EXPERT","PERF_DETAIL_NOVICE","PERF_DETAIL_WIZARD","PPDH_BROWSE_DLG_CONFIG_H","PPDH_BROWSE_DLG_CONFIG_H structure pointer [Perf]","_win32_pdh_browse_dlg_config_h_str","base.pdh_browse_dlg_config_h_str","pdh/PDH_BROWSE_DLG_CONFIG_H","pdh/PDH_BROWSE_DLG_CONFIG_HA","pdh/PDH_BROWSE_DLG_CONFIG_HW","pdh/PPDH_BROWSE_DLG_CONFIG_H","perf.pdh_browse_dlg_config_h_str"]
old-location: perf\pdh_browse_dlg_config_h_str.htm
tech.root: perf
ms.assetid: db30ff94-3238-45a0-a78e-8b3cd00ec79c
ms.date: 12/05/2018
ms.keywords: '*PPDH_BROWSE_DLG_CONFIG_HW, PDH_BROWSE_DLG_CONFIG_H, PDH_BROWSE_DLG_CONFIG_H structure [Perf], PDH_BROWSE_DLG_CONFIG_HA, PDH_BROWSE_DLG_CONFIG_HW, PERF_DETAIL_ADVANCED, PERF_DETAIL_EXPERT, PERF_DETAIL_NOVICE, PERF_DETAIL_WIZARD, PPDH_BROWSE_DLG_CONFIG_H, PPDH_BROWSE_DLG_CONFIG_H structure pointer [Perf], _win32_pdh_browse_dlg_config_h_str, base.pdh_browse_dlg_config_h_str, pdh/PDH_BROWSE_DLG_CONFIG_H, pdh/PDH_BROWSE_DLG_CONFIG_HA, pdh/PDH_BROWSE_DLG_CONFIG_HW, pdh/PPDH_BROWSE_DLG_CONFIG_H, perf.pdh_browse_dlg_config_h_str'
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PDH_BROWSE_DLG_CONFIG_HW (Unicode) and PDH_BROWSE_DLG_CONFIG_HA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PDH_BROWSE_DLG_CONFIG_HW, *PPDH_BROWSE_DLG_CONFIG_HW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BrowseDlgConfig_HW
 - pdh/_BrowseDlgConfig_HW
 - PPDH_BROWSE_DLG_CONFIG_HW
 - pdh/PPDH_BROWSE_DLG_CONFIG_HW
 - PDH_BROWSE_DLG_CONFIG_HW
 - pdh/PDH_BROWSE_DLG_CONFIG_HW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pdh.h
api_name:
 - PDH_BROWSE_DLG_CONFIG_H
 - PDH_BROWSE_DLG_CONFIG_HA
 - PDH_BROWSE_DLG_CONFIG_HW
---

# PDH_BROWSE_DLG_CONFIG_HW structure


## -description

The 
<b>PDH_BROWSE_DLG_CONFIG_H</b> structure is used by the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhbrowsecountersha">PdhBrowseCountersH</a> function to configure the <b>Browse Performance Counters</b> dialog box.

## -struct-fields

### -field bIncludeInstanceIndex

If this flag is <b>TRUE</b>, the dialog box includes an index number for duplicate instance names. For example, if there are two cmd instances, the instance list will contain cmd and cmd#1. If this flag is <b>FALSE</b>, duplicate instance names will not contain an index number.

### -field bSingleCounterPerAdd

If this flag is <b>TRUE</b>, the dialog returns only one counter. If this flag is <b>FALSE</b>, the dialog can return multiple selections, and wildcard selections are permitted. Selected counters are returned as a MULTI_SZ string.

### -field bSingleCounterPerDialog

If this flag is <b>TRUE</b>, the dialog box uses an OK and Cancel button. The dialog returns when the user clicks either button. If this flag is <b>FALSE</b>, the dialog box uses an Add and Close button. The dialog box closes when the user clicks the Close button. The Add button can be clicked multiple times. The Add button overwrites the previously selected items with the currently selected items.

### -field bLocalCountersOnly

If this flag is <b>TRUE</b>, the dialog box lets the user select counters only from the local computer (the path will not contain a computer name). If this flag is <b>FALSE</b>, the user can specify a computer from which to select counters. The computer name will prefix the counter path unless the user selects <b>Use local computer counters</b>.

### -field bWildCardInstances

If this flag is <b>TRUE</b> and the user selects <b>All instances</b>, the counter path will include the wildcard character for the instance field. 


If this flag is <b>FALSE</b>, and the user selects <b>All instances</b>, all the instances currently found for that object will be returned in a MULTI_SZ string.

### -field bHideDetailBox

If this flag is <b>TRUE</b>, this removes <b>Detail level</b> from the dialog box so the user cannot change the detail level of the counters displayed in the dialog box. The detail level will be fixed to the value of the <b>dwDefaultDetailLevel</b> member. 


If this flag is <b>FALSE</b>, this displays <b>Detail level</b> in the dialog box, allowing the user to change the detail level of the counters displayed. 



Note that the counters displayed will be those whose detail level is less than or equal to the current detail level selection. Selecting a detail level of Wizard will display all counters and objects.

### -field bInitializePath

If this flag is <b>TRUE</b>, the dialog highlights the counter and object specified in <b>szReturnPathBuffer</b> when the dialog box is first displayed, instead of using the default counter and object specified by the computer. 


If this flag is <b>FALSE</b>, this selects the initial counter and object using the default counter and object information returned by the computer.

### -field bDisableMachineSelection

If this flag is <b>TRUE</b>, the user cannot select a computer from  <b>Select counters from computer</b>. 


If this flag is <b>FALSE</b>, the user can select a computer from <b>Select counters from computer</b>. This is the default value. 
The list contains the local computer only unless you call the <a href="/windows/desktop/api/pdh/nf-pdh-pdhconnectmachinea">PdhConnectMachine</a> to connect to other computers first.

### -field bIncludeCostlyObjects

If this flag is <b>TRUE</b>, the counters list will also contain costly data—that is, data that requires a relatively large amount of processor time or memory overhead to collect. 


If this flag is <b>FALSE</b>, the list will not contain costly counters. This is the default value.

### -field bShowObjectBrowser

If this flag is <b>TRUE</b>, the dialog lists only performance objects. When the user selects an object, the dialog returns a counter path that includes the object and wildcard characters for the instance name and counter if the object is a multiple instance object. For example, if the "Process" object is selected, the dialog returns the string "\Process(*)\*". If the object is a single instance object, the path contains a wildcard character for counter only. For example, "\System\*". You can then pass the path to <a href="/windows/desktop/api/pdh/nf-pdh-pdhexpandwildcardpatha">PdhExpandWildCardPath</a> to retrieve a list of actual paths for the object.

### -field bReserved

### -field hWndOwner

Handle of the window to own the dialog. If <b>NULL</b>, the owner is the desktop.

### -field hDataSource

Handle to a data source returned by the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhbindinputdatasourcea">PdhBindInputDataSource</a> function.

### -field szReturnPathBuffer

Pointer to a MULTI_SZ that contains the selected counter paths. 

If <b>bInitializePath</b> is <b>TRUE</b>, you can use this member to specify a counter path whose components are used to highlight entries in computer, object, counter, and instance lists when the dialog is first displayed.

### -field cchReturnPathLength

Size of the <b>szReturnPathBuffer</b> buffer, in <b>TCHARs</b>. If the callback function reallocates a new buffer, it must also update this value.

### -field pCallBack

Pointer to the callback function that processes the user's selection. For more information, see 
<a href="/windows/desktop/api/pdh/nc-pdh-counterpathcallback">CounterPathCallBack</a>.

### -field dwCallBackArg

Caller-defined value that is passed to the callback function.

### -field CallBackStatus

On entry to the callback function, this member contains the status of the path buffer. On exit, the callback function sets the status value resulting from processing. 




If the buffer is too small to load the current selection, the dialog sets this value to PDH_MORE_DATA. If this value is ERROR_SUCCESS, then the <b>szReturnPathBuffer</b> member contains a valid counter path or counter path list.

If the callback function reallocates a new buffer, it should set this member to PDH_RETRY so that the dialog will try to load the buffer with the selected paths and call the callback function again.

If some other error occurred, then the callback function should return the appropriate PDH error status value.

### -field dwDefaultDetailLevel

Default detail level to show in the <b>Detail level</b> list if <b>bHideDetailBox</b> is <b>FALSE</b>. If <b>bHideDetailBox</b> is <b>TRUE</b>, the dialog uses this value to filter the displayed performance counters and objects. You can specify one of the following values:

<table>
<tr>
<th>Detail level</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PERF_DETAIL_NOVICE"></a><a id="perf_detail_novice"></a><dl>
<dt><b>PERF_DETAIL_NOVICE</b></dt>
</dl>
</td>
<td width="60%">
A novice user can understand the counter data.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_DETAIL_ADVANCED"></a><a id="perf_detail_advanced"></a><dl>
<dt><b>PERF_DETAIL_ADVANCED</b></dt>
</dl>
</td>
<td width="60%">
The counter data is provided for advanced users.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_DETAIL_EXPERT"></a><a id="perf_detail_expert"></a><dl>
<dt><b>PERF_DETAIL_EXPERT</b></dt>
</dl>
</td>
<td width="60%">
The counter data is provided for expert users.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_DETAIL_WIZARD"></a><a id="perf_detail_wizard"></a><dl>
<dt><b>PERF_DETAIL_WIZARD</b></dt>
</dl>
</td>
<td width="60%">
The counter data is provided for system designers.

</td>
</tr>
</table>

### -field szDialogBoxCaption

Pointer to a <b>null</b>-terminated string that specifies the optional caption to display in the caption bar of the dialog box. If this member is <b>NULL</b>, the caption will be <b>Browse Performance Counters</b>.

## -remarks

Each time the 
<a href="/windows/desktop/SysMon/counters-add">Add</a> button is clicked, the <b>szReturnPathBuffer</b> buffer contains the selected counter and the <b>pCallBack</b> callback function is called. The callback function should call the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhaddcountera">PdhAddCounter</a> function for each counter in the buffer.





> [!NOTE]
> The pdh.h header defines PDH_BROWSE_DLG_CONFIG_H as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/pdh/nc-pdh-counterpathcallback">CounterPathCallBack</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhaddcountera">PdhAddCounter</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhbindinputdatasourcea">PdhBindInputDataSource</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhbrowsecountersha">PdhBrowseCountersH</a>
