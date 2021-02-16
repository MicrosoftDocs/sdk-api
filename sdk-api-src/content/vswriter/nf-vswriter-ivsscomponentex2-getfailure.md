---
UID: NF:vswriter.IVssComponentEx2.GetFailure
title: IVssComponentEx2::GetFailure (vswriter.h)
description: VSS requesters call this method to retrieve component-level errors reported by writers.
helpviewer_keywords: ["GetFailure","GetFailure method","GetFailure method","IVssComponentEx2 interface","IVssComponentEx2 interface","GetFailure method","IVssComponentEx2.GetFailure","IVssComponentEx2::GetFailure","S_OK","VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT","VSS_E_WRITERERROR_NONRETRYABLE","VSS_E_WRITERERROR_OUTOFRESOURCES","VSS_E_WRITERERROR_RETRYABLE","VSS_E_WRITERERROR_TIMEOUT","VSS_E_WRITER_NOT_RESPONDING","VSS_E_WRITER_STATUS_NOT_AVAILABLE","base.ivsscomponentex2_getfailure","vswriter/IVssComponentEx2::GetFailure"]
old-location: base\ivsscomponentex2_getfailure.htm
tech.root: base
ms.assetid: a5d739d3-9169-4b25-a590-35703e77dacc
ms.date: 12/05/2018
ms.keywords: GetFailure, GetFailure method, GetFailure method,IVssComponentEx2 interface, IVssComponentEx2 interface,GetFailure method, IVssComponentEx2.GetFailure, IVssComponentEx2::GetFailure, S_OK, VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT, VSS_E_WRITERERROR_NONRETRYABLE, VSS_E_WRITERERROR_OUTOFRESOURCES, VSS_E_WRITERERROR_RETRYABLE, VSS_E_WRITERERROR_TIMEOUT, VSS_E_WRITER_NOT_RESPONDING, VSS_E_WRITER_STATUS_NOT_AVAILABLE, base.ivsscomponentex2_getfailure, vswriter/IVssComponentEx2::GetFailure
req.header: vswriter.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssComponentEx2::GetFailure
 - vswriter/IVssComponentEx2::GetFailure
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - vswriter.h
api_name:
 - IVssComponentEx2.GetFailure
---

# IVssComponentEx2::GetFailure


## -description

VSS requesters call this method to retrieve component-level errors reported by writers.

## -parameters

### -param phr [out]

The address of a caller-allocated variable that receives the HRESULT failure code that the writer passed for the <i>hr</i> parameter of the <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex2-setfailure">IVssComponentEx2::SetFailure</a> method. This parameter is required and cannot be <b>NULL</b>.

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
</table>

### -param phrApplication [out]

The address of a caller-allocated variable that receives the return code that the writer passed for the <i>hrApplication</i> parameter of  the <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex2-setfailure">SetFailure</a> method. This parameter is required and cannot be <b>NULL</b>.

### -param pbstrApplicationMessage [out]

The address of a caller-allocated variable that receives the application failure message that the writer passed for the <i>wszApplicationMessage</i> parameter of the <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex2-setfailure">SetFailure</a> method. This parameter is required and cannot be <b>NULL</b>.

### -param pdwReserved [out]

The address of a caller-allocated DWORD variable. This parameter is reserved for future use, but it is required and cannot be <b>NULL</b>.

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
The <i>phr</i>, <i>phrApplication</i>, <i>pbstrApplicationMessage</i>, or <i>pdwReserved</i> parameter is <b>NULL</b>.

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
</table>

## -remarks

When the caller has finished accessing the status information returned by this method, it should call 
    <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory held by the  <i>pbstrApplicationMessage</i> parameter.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponentex2">IVssComponentEx2</a>