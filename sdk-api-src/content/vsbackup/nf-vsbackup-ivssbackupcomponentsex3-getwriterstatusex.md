---
UID: NF:vsbackup.IVssBackupComponentsEx3.GetWriterStatusEx
title: IVssBackupComponentsEx3::GetWriterStatusEx (vsbackup.h)
description: Returns extended status information for the specified writer.
helpviewer_keywords: ["GetWriterStatusEx","GetWriterStatusEx method","GetWriterStatusEx method","IVssBackupComponentsEx3 interface","IVssBackupComponentsEx3 interface","GetWriterStatusEx method","IVssBackupComponentsEx3.GetWriterStatusEx","IVssBackupComponentsEx3::GetWriterStatusEx","S_OK","VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT","VSS_E_WRITERERROR_NONRETRYABLE","VSS_E_WRITERERROR_OUTOFRESOURCES","VSS_E_WRITERERROR_PARTIAL_FAILURE","VSS_E_WRITERERROR_RETRYABLE","VSS_E_WRITERERROR_TIMEOUT","VSS_E_WRITER_NOT_RESPONDING","VSS_E_WRITER_STATUS_NOT_AVAILABLE","base.ivssbackupcomponentsex3_getwriterstatusex","vsbackup/IVssBackupComponentsEx3::GetWriterStatusEx"]
old-location: base\ivssbackupcomponentsex3_getwriterstatusex.htm
tech.root: base
ms.assetid: ab2be2c0-04bb-4a56-a636-ebd2c06e844a
ms.date: 12/05/2018
ms.keywords: GetWriterStatusEx, GetWriterStatusEx method, GetWriterStatusEx method,IVssBackupComponentsEx3 interface, IVssBackupComponentsEx3 interface,GetWriterStatusEx method, IVssBackupComponentsEx3.GetWriterStatusEx, IVssBackupComponentsEx3::GetWriterStatusEx, S_OK, VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT, VSS_E_WRITERERROR_NONRETRYABLE, VSS_E_WRITERERROR_OUTOFRESOURCES, VSS_E_WRITERERROR_PARTIAL_FAILURE, VSS_E_WRITERERROR_RETRYABLE, VSS_E_WRITERERROR_TIMEOUT, VSS_E_WRITER_NOT_RESPONDING, VSS_E_WRITER_STATUS_NOT_AVAILABLE, base.ivssbackupcomponentsex3_getwriterstatusex, vsbackup/IVssBackupComponentsEx3::GetWriterStatusEx
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssBackupComponentsEx3::GetWriterStatusEx
 - vsbackup/IVssBackupComponentsEx3::GetWriterStatusEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsBackup.h
api_name:
 - IVssBackupComponentsEx3.GetWriterStatusEx
---

# IVssBackupComponentsEx3::GetWriterStatusEx


## -description

Returns extended status information for the specified writer.

## -parameters

### -param iWriter [in]

The index of the writer whose metadata is to be retrieved. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of 
      writers on the current system. The value of <i>n</i> is returned by 
      the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount">IVssBackupComponents::GetWriterStatusCount</a> method.

### -param pidInstance [out]

The address of a caller-allocated variable that receives the instance identifier of the writer. This parameter is required and cannot be <b>NULL</b>.

### -param pidWriter [out]

The address of a caller-allocated variable that receives the identifier for the writer class. This parameter is required and cannot be <b>NULL</b>.

### -param pbstrWriter [out]

The address of a caller-allocated variable that receives a string containing the name of the specified writer. This parameter is required and cannot be <b>NULL</b>.

### -param pnStatus [out]

The address of a caller-allocated variable that receives a <a href="/windows/desktop/api/vss/ne-vss-vss_writer_state">VSS_WRITER_STATE</a> enumeration value. This parameter is required and cannot be <b>NULL</b>.

### -param phrFailureWriter [out]

The address of a caller-allocated variable that receives the HRESULT failure code that the writer returned for the <i>hrWriter</i> parameter of the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-setwriterfailureex">CVssWriterEx2::SetWriterFailureEx</a> method. 
      

The following are the supported values.

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
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

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

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_PARTIAL_FAILURE"></a><a id="vss_e_writererror_partial_failure"></a><dl>
<dt><b>VSS_E_WRITERERROR_PARTIAL_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The writer is reporting one or more component-level errors. To retrieve the errors, the requester must use the <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex2-getfailure">IVssComponentEx2::GetFailure</a> method.

</td>
</tr>
</table>

### -param phrApplication [out, optional]

The address of a caller-allocated variable that receives the return code that the writer passed for the <i>hrApplication</i> parameter of  the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-setwriterfailureex">CVssWriterEx2::SetWriterFailureEx</a> method. This parameter is optional and can be <b>NULL</b>.

### -param pbstrApplicationMessage [out, optional]

The address of a variable that receives the application failure message that the writer passed for the <i>wszApplicationMessage</i> parameter of the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-setwriterfailureex">SetWriterFailureEx</a> method. This parameter is optional and can be <b>NULL</b>.

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
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Successfully returned the status of the specified writer. Note that the value of the 
        <i>phrFailureWriter</i> parameter must be checked to verify that the writer was successful. 
        The writer failure codes can be among those listed in VsWriter.h and in <a href="/windows/desktop/VSS/writer-errors-and-vetoes">Writer Errors and Vetoes</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057L</dt>
</dl>
</td>
<td width="60%">
The <i>pnStatus</i>, <i>pidWriter</i>, <i>pbstrWriter</i>, or <i>pidInstance</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
<dt>0x8007000EL</dt>
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
<dt>0x80042301L</dt>
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
<dt>0x80042308L</dt>
</dl>
</td>
<td width="60%">
The <i>iWriter</i> parameter specifies a writer that does not exist.

</td>
</tr>
</table>

## -remarks

A requester must call the asynchronous operation 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus">IVssBackupComponents::GatherWriterStatus</a> 
    and wait for it to complete before calling 
    <b>IVssBackupComponentsEx3::GetWriterStatusEx</b>.

If this method returns VSS_E_WRITERERROR_PARTIAL_FAILURE, the requester should use the <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex2-getfailure">IVssComponentEx2::GetFailure</a> method to retrieve the component-level errors.

When the caller has finished accessing the status information returned by this method, it should call 
    <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory held by the 
    <i>pbstrWriter</i> and <i>pbstrApplicationMessage</i> parameters.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-setwriterfailureex">CVssWriterEx2::SetWriterFailureEx</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus">IVssBackupComponents::GetWriterStatus</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex3">IVssBackupComponentsEx3</a>