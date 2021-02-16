---
UID: NF:vsbackup.IVssBackupComponents.GetWriterStatus
title: IVssBackupComponents::GetWriterStatus (vsbackup.h)
description: The GetWriterStatus method returns the status of the specified writer.
helpviewer_keywords: ["GetWriterStatus","GetWriterStatus method [VSS]","GetWriterStatus method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","GetWriterStatus method","IVssBackupComponents.GetWriterStatus","IVssBackupComponents::GetWriterStatus","S_OK","VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT","VSS_E_WRITERERROR_NONRETRYABLE","VSS_E_WRITERERROR_OUTOFRESOURCES","VSS_E_WRITERERROR_RETRYABLE","VSS_E_WRITERERROR_TIMEOUT","VSS_E_WRITER_NOT_RESPONDING","VSS_E_WRITER_STATUS_NOT_AVAILABLE","_win32_ivssbackupcomponents_getwriterstatus","base.ivssbackupcomponents_getwriterstatus","vsbackup/IVssBackupComponents::GetWriterStatus"]
old-location: base\ivssbackupcomponents_getwriterstatus.htm
tech.root: base
ms.assetid: 652e9630-291d-41cd-96d9-6a63988932a5
ms.date: 12/05/2018
ms.keywords: GetWriterStatus, GetWriterStatus method [VSS], GetWriterStatus method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],GetWriterStatus method, IVssBackupComponents.GetWriterStatus, IVssBackupComponents::GetWriterStatus, S_OK, VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT, VSS_E_WRITERERROR_NONRETRYABLE, VSS_E_WRITERERROR_OUTOFRESOURCES, VSS_E_WRITERERROR_RETRYABLE, VSS_E_WRITERERROR_TIMEOUT, VSS_E_WRITER_NOT_RESPONDING, VSS_E_WRITER_STATUS_NOT_AVAILABLE, _win32_ivssbackupcomponents_getwriterstatus, base.ivssbackupcomponents_getwriterstatus, vsbackup/IVssBackupComponents::GetWriterStatus
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssBackupComponents::GetWriterStatus
 - vsbackup/IVssBackupComponents::GetWriterStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssBackupComponents.GetWriterStatus
---

# IVssBackupComponents::GetWriterStatus


## -description

The <b>GetWriterStatus</b> method 
   returns the status of the specified writer.

## -parameters

### -param iWriter [in]

Index of the writer whose metadata is to be retrieved. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of 
      writers on the current system. The value of <i>n</i> is returned by 
      <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount">IVssBackupComponents::GetWriterStatusCount</a>.

### -param pidInstance [out]

The address of a caller-allocated variable that receives the instance identifier of the writer.

### -param pidWriter [out]

The address of a caller-allocated variable that receives the identifier for the writer class.

### -param pbstrWriter [out]

The address of a caller-allocated variable that receives a string containing the name of the specified writer.

### -param pnStatus [out]

The address of a caller-allocated variable that receives a <a href="/windows/desktop/api/vss/ne-vss-vss_writer_state">VSS_WRITER_STATE</a> enumeration value.

### -param phResultFailure [out]

The address of a caller-allocated variable that receives the HRESULT failure code that was returned by the writer. 
      

The following are the supported values for <i>pHrResultFailure</i>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="S_OK"></a><a id="s_ok"></a><dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The writer was successful.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT"></a><a id="vss_e_writererror_inconsistentsnapshot"></a><dl>
<dt><b>VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT</b></dt>
</dl>
</td>
<td width="60%">
The shadow copy contains only a subset of the volumes needed by the writer to correctly back up the 
        application component.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_OUTOFRESOURCES"></a><a id="vss_e_writererror_outofresources"></a><dl>
<dt><b>VSS_E_WRITERERROR_OUTOFRESOURCES</b></dt>
</dl>
</td>
<td width="60%">
The writer ran out of memory or other system resources. The recommended way to handle this error code is 
        to wait ten minutes and then repeat the operation, up to three times.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_TIMEOUT"></a><a id="vss_e_writererror_timeout"></a><dl>
<dt><b>VSS_E_WRITERERROR_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The writer operation failed because of a time-out between the Freeze and Thaw events. The recommended way 
        to handle this error code is to wait ten minutes and then repeat the operation, up to three times.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_RETRYABLE"></a><a id="vss_e_writererror_retryable"></a><dl>
<dt><b>VSS_E_WRITERERROR_RETRYABLE</b></dt>
</dl>
</td>
<td width="60%">
The writer failed due to an error that would likely not occur if the entire backup, restore, or shadow 
        copy creation process was restarted. The recommended way to handle this error code is to wait ten minutes and 
        then repeat the operation, up to three times.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_NONRETRYABLE"></a><a id="vss_e_writererror_nonretryable"></a><dl>
<dt><b>VSS_E_WRITERERROR_NONRETRYABLE</b></dt>
</dl>
</td>
<td width="60%">
The writer operation failed because of an error that might recur if another shadow copy is created. For 
        more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error 
        Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITER_NOT_RESPONDING"></a><a id="vss_e_writer_not_responding"></a><dl>
<dt><b>VSS_E_WRITER_NOT_RESPONDING</b></dt>
</dl>
</td>
<td width="60%">
The writer is not responding.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITER_STATUS_NOT_AVAILABLE"></a><a id="vss_e_writer_status_not_available"></a><dl>
<dt><b>VSS_E_WRITER_STATUS_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The writer status is not available for one or more writers. A writer may have reached the maximum number of available backup and restore sessions. 

<b>Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
</table>

## -returns

The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully returned the status of the specified writer. Note that the value of the 
        <i>pHrWriterFailure</i> parameter must be checked to verify that the writer was successful. 
        The writer failure codes can be among those listed in VsWriter.h and in <a href="/windows/desktop/VSS/writer-errors-and-vetoes">Writer Errors and Vetoes</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The backup components object is not initialized, this method has been called during a restore operation, 
        or this method has not been called within the correct sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified writer does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>

## -remarks

A requester must call the asynchronous operation 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus">IVssBackupComponents::GatherWriterStatus</a> 
    and wait for it to complete prior to calling 
    <b>GetWriterStatus</b>.

When the caller has finished accessing the status information returned by this method, it should call 
    <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory held by the 
    <i>pbstrWriter</i> parameter.

The VSS_E_WRITERERROR_<i>XXX</i> values returned in the <i>pHrResultFailure</i> parameter are generated by writers. VSS_E_WRITER_NOT_RESPONDING and VSS_E_WRITER_STATUS_NOT_AVAILABLE are generated by VSS.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus">IVssBackupComponents::GatherWriterStatus</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount">IVssBackupComponents::GetWriterStatusCount</a>