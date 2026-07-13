---
UID: NF:setupapi.SetupScanFileQueueA
title: SetupScanFileQueueA function (setupapi.h)
description: The SetupScanFileQueue function scans a setup file queue, performing an operation on each node in its copy list. The operation is specified by a set of flags. This function can be called either before or after the queue has been committed. (ANSI)
helpviewer_keywords: ["SPQ_SCAN_FILE_PRESENCE", "SPQ_SCAN_FILE_VALIDITY", "SPQ_SCAN_INFORM_USER", "SPQ_SCAN_PRUNE_COPY_QUEUE", "SPQ_SCAN_PRUNE_DELREN", "SPQ_SCAN_USE_CALLBACK", "SPQ_SCAN_USE_CALLBACKEX", "SPQ_SCAN_USE_CALLBACK_SIGNERINFO", "SetupScanFileQueueA", "setupapi/SetupScanFileQueueA"]
old-location: setup\setupscanfilequeue.htm
tech.root: setup
ms.assetid: 4d59bb19-bb4a-4a24-814b-322e46e40fab
ms.date: 12/05/2018
ms.keywords: SPQ_SCAN_FILE_PRESENCE, SPQ_SCAN_FILE_VALIDITY, SPQ_SCAN_INFORM_USER, SPQ_SCAN_PRUNE_COPY_QUEUE, SPQ_SCAN_PRUNE_DELREN, SPQ_SCAN_USE_CALLBACK, SPQ_SCAN_USE_CALLBACKEX, SPQ_SCAN_USE_CALLBACK_SIGNERINFO, SetupScanFileQueue, SetupScanFileQueue function [Setup API], SetupScanFileQueueA, SetupScanFileQueueW, _setupapi_setupscanfilequeue, setup.setupscanfilequeue, setupapi/SetupScanFileQueue, setupapi/SetupScanFileQueueA, setupapi/SetupScanFileQueueW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupScanFileQueueW (Unicode) and SetupScanFileQueueA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupScanFileQueueA
 - setupapi/SetupScanFileQueueA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupScanFileQueue
 - SetupScanFileQueueA
 - SetupScanFileQueueW
---

# SetupScanFileQueueA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupScanFileQueue</b> function scans a setup file queue, performing an operation on each node in its copy list. The operation is specified by a set of flags. This function can be called either before or after the queue has been committed.

## -parameters

### -param FileQueue [in]

Handle to the setup file queue whose copy list is to be scanned or iterated.

### -param Flags [in]

Flags to combine to control the file queue scan operation. Note that either SPQ_SCAN_FILE_PRESENCE, SPQ_SCAN_USE_CALLBACK, SPQ_SCAN_USE_CALLBACKEX, or SPQ_SCAN_FILE_VALIDITY must be specified. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPQ_SCAN_FILE_PRESENCE"></a><a id="spq_scan_file_presence"></a><dl>
<dt><b>SPQ_SCAN_FILE_PRESENCE</b></dt>
</dl>
</td>
<td width="60%">
Target files in the copy queue  are already present on the target.

</td>
</tr>
<tr>
<td width="40%"><a id="SPQ_SCAN_FILE_VALIDITY"></a><a id="spq_scan_file_validity"></a><dl>
<dt><b>SPQ_SCAN_FILE_VALIDITY</b></dt>
</dl>
</td>
<td width="60%">
Target files in the copy queue  are already present on the target with valid signatures. Available  with Windows 2000 and later versions.

</td>
</tr>
<tr>
<td width="40%"><a id="SPQ_SCAN_USE_CALLBACK"></a><a id="spq_scan_use_callback"></a><dl>
<dt><b>SPQ_SCAN_USE_CALLBACK</b></dt>
</dl>
</td>
<td width="60%">
Callback routine for each node of the queue. If the callback routine returns a nonzero value, the queue processing stops and 
<b>SetupScanFileQueue</b> returns zero. Issue a 
<a href="/windows/desktop/SetupApi/spfilenotify-queuescan">SPFILENOTIFY_QUEUESCAN</a> notification code and a pass a pointer to the target path as <i>Param1</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPQ_SCAN_USE_CALLBACKEX"></a><a id="spq_scan_use_callbackex"></a><dl>
<dt><b>SPQ_SCAN_USE_CALLBACKEX</b></dt>
</dl>
</td>
<td width="60%">
Callback routine for each node of the queue. If the callback routine returns a nonzero value, the queue processing stops and 
<b>SetupScanFileQueue</b> returns zero. Issue a SPFILENOTIFY_QUEUESCAN_EX notification and pass a pointer to a 
<a href="/windows/desktop/api/setupapi/ns-setupapi-filepaths_a">FILEPATHS</a> structure as <i>Param1</i>. SPQ_SCAN_USE_CALLBACKEX also checks that the file has a valid signature. Available starting with Windows 2000. On Windows XP only, you can turn off signature checking by combining this flag with SPQ_SCAN_FILE_PRESENCE.

</td>
</tr>
<tr>
<td width="40%"><a id="SPQ_SCAN_INFORM_USER"></a><a id="spq_scan_inform_user"></a><dl>
<dt><b>SPQ_SCAN_INFORM_USER</b></dt>
</dl>
</td>
<td width="60%">
Flag  specified when all  files in the queue pass the check for valid signatures. 
<b>SetupScanFileQueue</b> informs the user that the operation requires files that are already present on the target. This flag is ignored if SPQ_SCAN_FILE_PRESENCE or SPQ_SCAN_FILE_VALIDITY is not specified. This flag may not be used with SPQ_SCAN_PRUNE_COPY_QUEUE or SPQ_SCAN_PRUNE_DELREN.

</td>
</tr>
<tr>
<td width="40%"><a id="SPQ_SCAN_PRUNE_COPY_QUEUE"></a><a id="spq_scan_prune_copy_queue"></a><dl>
<dt><b>SPQ_SCAN_PRUNE_COPY_QUEUE</b></dt>
</dl>
</td>
<td width="60%">
Combined with SPQ_SCAN_FILE_PRESENCE, removes present entries from the copy queue. When combined with SPQ_SCAN_FILE_VALIDITY, removes signed entries from the copy queue. Available starting with Windows 2000. On Windows XP only, files that are also specified in the delete queue or rename queues are not pruned unless SPQ_SCAN_PRUNE_DELREN is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="SPQ_SCAN_USE_CALLBACK_SIGNERINFO"></a><a id="spq_scan_use_callback_signerinfo"></a><dl>
<dt><b>SPQ_SCAN_USE_CALLBACK_SIGNERINFO</b></dt>
</dl>
</td>
<td width="60%">
Available starting with Windows XP. Issues SPFILENOTIFY_QUEUESCAN_SIGNERINFO notification and passes a pointer to a 
<a href="/windows/desktop/api/setupapi/ns-setupapi-filepaths_signerinfo_a">FILEPATHS_SIGNERINFO</a> structure as <i>Param1</i>. Checks each file for a valid signature and reports signature information through the callback function.

</td>
</tr>
<tr>
<td width="40%"><a id="SPQ_SCAN_PRUNE_DELREN"></a><a id="spq_scan_prune_delren"></a><dl>
<dt><b>SPQ_SCAN_PRUNE_DELREN</b></dt>
</dl>
</td>
<td width="60%">
Combined with SPQ_SCAN_FILE_PRESENCE or SPQ_SCAN_FILE_VALIDITY, removes entries in the delete  or rename queue that are also in the copy queue. When combined with SPQ_SCAN_PRUNE_COPY_QUEUE, limits files that are removed from the copy queue to files that are not in  the delete  or  rename queues. Available starting with Windows XP.

</td>
</tr>
</table>

### -param Window [in]

Optional handle to the window to own dialog boxes that are presented. This parameter is not used if the <i>Flags</i> parameter does not contain SPQ_SCAN_FILE_PRESENCE or if <i>Flags</i> does not contain SPQ_SCAN_INFORM_USER.

### -param CallbackRoutine [in]

Optional pointer to a <a href="/windows/desktop/api/setupapi/nc-setupapi-psp_file_callback_a">FileCallback</a> callback function to be called on each node of the copy queue. The notification code passed to the callback function is 
<a href="/windows/desktop/SetupApi/spfilenotify-queuescan">SPFILENOTIFY_QUEUESCAN</a>. This parameter is required if <i>Flags</i> includes SPQ_SCAN_USE_CALLBACK. 




<div class="alert"><b>Note</b>  You must supply the callback routine specified by <i>CallbackRoutine</i>. The default queue callback routine does not support 
<b>SetupScanFileQueue</b>.</div>
<div> </div>

### -param CallbackContext [in]

Optional pointer to a context that contains caller-defined data passed to the callback routine pointed to by <i>CallbackRoutine</i>.

### -param Result [out]

Pointer to a variable that receives the result of the scan operation.

## -returns

The function returns a nonzero value if all nodes in the queue were processed.

If the SPQ_SCAN_USE_CALLBACK flag was set, the value in <i>Result</i> is 0. The callback routine specified by <i>CallbackRoutine</i> is sent the notification SPFILENOTIFY_QUEUESCAN. <i>CallbackRoutine.Param1</i> specifies a pointer to an array that contains the target path information. The pointer has been cast to an unsigned integer and must be recast to a TCHAR array of MAX_PATH elements before a callback routine can access the information. <i>CallbackRoutine.Param2</i> is set to SPQ_DELAYED_COPY if the current queue node is in use and cannot be copied until the system is restarted. Otherwise, <i>CallbackRoutine.Param2</i> takes the value 0.

If SPQ_SCAN_USE_CALLBACK was not set, <i>Result</i> indicates whether the queue passed the presence or validity check as shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The queue failed the check or it passed the check, but SPQ_SCAN_INFORM_USER was specified and the user wants new copies of the files.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
The queue passed the check and, if SPQ_SCAN_INFORM_USER was specified, the user indicated that copying is not required. The copy queue is empty and there are no elements on the delete or rename queues, so the caller can skip queue commit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
The queue passed the check and, if SPQ_SCAN_INFORM_USER was specified, the user indicated that copying is not required. The copy queue is empty, but there are elements on the delete or rename queues, so the caller cannot skip queue commit.

</td>
</tr>
</table>
 

The function returns zero if an error occurred or the callback function returned nonzero. If <i>Result</i> is nonzero, it is the value returned by the callback function that stopped queue processing. If <i>Result</i> is zero, extended error information can be retrieved by a call to 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nc-setupapi-psp_file_callback_a">FileCallback</a>



<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupcommitfilequeuea">SetupCommitFileQueue</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdefaultqueuecallbacka">SetupDefaultQueueCallback</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupScanFileQueue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
